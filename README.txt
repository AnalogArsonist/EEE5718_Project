This archive contains an ipython3 notebook file (EEE5718_Project.ipynb) that can be ran using ipython3 or viewed on github: https://github.com/AnalogArsonist

The tst.ts file is the input MPEG-2 TS file that is defined as the source, although any .ts file will work.

The inner_decode_output_1.ts and inner_decode_output_9.ts files are generated from the accompanied Matlab code. The files were orginally generated at the outer coding block output in this python script. The files were then sent to the Matlab code as an input to the inner coding blocks. The data was then sent through a noisy link and recovered by the inner decoder. The output of that decoder was then re-imported into python as an input to the outer decoder block. The file then went through the de-scrambler where it is finally compared to the origin bistream from tst.ts. This is a full end to end simulation when using the inner coding from matlab.

Certain flags can be set to enable verbose mode (lots of text) or to enable plots. The loop can also be adjusted to set how many frames are used to check the BER. The SNR can also be set and ran for multiple values by setting SNRr to a list, i.e., [1,2,3,4,5]. The values are in dB. Outer coding can be disabled with a flag as well, and the import of inner coding data from matlab can also be set. 
