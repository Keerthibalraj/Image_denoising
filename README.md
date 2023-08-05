# Image_denoising

# *Gaussian*
The Gaussian filter is a commonly used method for image denoising. It is a linear filter that works by applying a weighted average to the pixel values in the image, with the weights determined by a Gaussian kernel. The Gaussian filter is effective at removing Gaussian noise from the image while preserving edges and important features. The Gaussian filter's kernel is a two-dimensional matrix with values following the Gaussian distribution. The size of the kernel and the standard deviation (σ) of the Gaussian determine the amount of smoothing applied to the image. A larger kernel and higher σ value result in more aggressive smoothing, which can effectively remove noise but might blur the image details.

The formula for a 2D Gaussian kernel centered at (0, 0) is given by:

G(x, y) = (1 / (2 * π * σ^2)) * exp(-(x^2 + y^2) / (2 * σ^2))

Where:

G(x, y) is the value at position (x, y) in the Gaussian kernel.
π is the mathematical constant pi (approximately 3.14159).
σ is the standard deviation of the Gaussian distribution, controlling the width of the Gaussian curve.
# *Non-Local Means*
The non-local means (NLM) filter is a powerful image denoising technique that goes beyond local pixel neighborhoods to estimate the clean image's denoised version. Unlike local filters that only consider a small window around each pixel, the NLM filter takes into account the similarities between patches of pixels from all over the image to perform denoising.Mathematically, the denoised value I_denoised(x, y) for a pixel at position (x, y) in the image can be expressed as:

I_denoised(x, y) = Σ w(x, y, i, j) * I_noisy(i, j) / Σ w(x, y, i, j)

Where:

w(x, y, i, j) represents the weight of the pixel at position (i, j) in the search window for the denoising of the pixel at (x, y).
I_noisy(i, j) is the pixel value at position (i, j) in the noisy input image.
# *Median filter*
The median filter is a popular non-linear image denoising technique that effectively removes impulse noise, also known as salt-and-pepper noise, from digital images. Unlike linear filters (e.g., Gaussian filter), the median filter is non-linear and does not blur the image edges and details. Instead, it replaces the central pixel value with the median value of the pixel intensities within a local neighborhood.
# *Bilateral filter*
The bilateral filter is a non-linear edge-preserving image denoising technique that effectively reduces noise while preserving the edges and details in the image. It achieves this by incorporating both spatial and intensity information when filtering the image. The filter considers neighboring pixels in both space and intensity domains and applies weights based on the similarity between pixels to perform denoising.
# *Total variation*
Total variation (TV) is a widely used method for image denoising. It is a mathematical concept that measures the variation or differences between adjacent pixel values in an image. The underlying idea is that images with smooth regions tend to have small variations between neighboring pixels, while noisy images have higher variations.The objective function typically takes the form of:

min ||I - I_noisy||^2 + λ * TV(I)

Where:

I is the denoised image.
I_noisy is the input noisy image.
λ is a parameter that controls the trade-off between denoising and preserving image features. Higher values of λ encourage stronger denoising but may lead to loss of details.
# *Autoencoders*
