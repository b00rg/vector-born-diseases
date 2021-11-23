import os
import random
from scipy import ndarray
import numpy as np
import skimage as sk
from skimage import io, exposure, transform, util
from skimage.transform import warp, AffineTransform, ProjectiveTransform
from skimage.exposure import equalize_adapthist, equalize_hist, rescale_intensity, adjust_gamma, adjust_log, adjust_sigmoid
from skimage.filters import gaussian, median
from skimage.util import random_noise
from PIL import Image, ImageFilter
import glob

old_folder = r"C:#path"
new_folder = r"C:#path\%s"
no_img_aug = 0

def Gamma1(image):
    return adjust_gamma(image,0.999999,1.01)

def Gamma2(image):
    return adjust_gamma(image,.05,5)

def Gamma3(image):
    return adjust_gamma(image,2)

def adjustLog(image):
    return adjust_log(image,0.2)

def adjustLog1(image):
    return adjust_log(image,0.5)

def adjustSigmoid(image):
    return adjust_sigmoid(image, 0.4)

def adjustSigmoid1(image):
    return adjust_sigmoid(image, 0.5)

filenames = glob.glob(os.path.join(os.sep, "C:" + os.sep, old_folder + os.sep, "*.jpg"))
images = [Image.open(img) for img in filenames]

for img in images:

    # raw file
    image_jpg = img.copy()
    image_jpg.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1
    
    # gamma ver 1
    image_jpg1 = img.copy()
    image_array1 = np.array(image_jpg1)
    gamma_corrected_array1 = Gamma1(image_array1)
    gamma_corrected_jpg1 = Image.fromarray(gamma_corrected_array1)
    gamma_corrected_jpg1.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1
    
    # gamma ver 2
    image_jpg2 = img.copy()
    image_array2 = np.array(image_jpg2)
    gamma_corrected_array2 = Gamma2(image_array2)
    check_array2 = image_array2 - gamma_corrected_array2
    gamma_corrected_jpg2 = Image.fromarray(gamma_corrected_array2)
    gamma_corrected_jpg2.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1

    # gamma ver 3
    image_jpg3 = img.copy()
    image_array3 = np.array(image_jpg3)
    gamma_corrected_array3 = Gamma3(image_array3)
    gamma_corrected_jpg3 = Image.fromarray(gamma_corrected_array3)
    gamma_corrected_jpg3.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1
    
    # log correction ver 1
    image_jpg111 = img.copy()
    image_array111 = np.array(image_jpg111)
    logCorrectArray = adjustLog(image_array3)
    logCorrectJpg = Image.fromarray(logCorrectArray)
    logCorrectJpg.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1
    
    #log correction ver 2
    image_jpg4 = img.copy()
    image_array4 = np.array(image_jpg4)
    logCorrectArray1 = adjustLog1(image_array4)
    logCorrectJpg1 = Image.fromarray(logCorrectArray1)
    logCorrectJpg1.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1
    
    
    # Gaussian Blur
    im7 = img.copy()
    im7_aug = im7.filter(ImageFilter.GaussianBlur(2))
    im7_aug.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1
    
    # noise
    im8 = img.copy()
    im8 = im8.effect_spread(1000)
    im8.save(new_folder % no_img_aug + '.jpg', 'JPEG')
    no_img_aug = no_img_aug + 1
    
    
   


