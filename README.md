## YOLOv7_ViT_MHSA

The Repository changes the BackBone `ELAN_Darknet` of YOLOv7 by adding `self-attention method` on the last BackBone layer.

I refered the codes of `ViT (Vision Transformer)` and remove the MLP layer.

Original code from rwightman and WZMIAOMIAO, below links are their Repositories.

```
https://github.com/rwightman/pytorch-image-models/blob/master/timm/models/vision_transformer.py
https://github.com/WZMIAOMIAO/deep-learning-for-image-processing
```

*Google Colab sometimes cannot run successfully with this Repository(changed from Bubliiiing's Codes).*

*Change pytorch version in 1.7.1 will help, i fix it in 2022.09. Good Luck!*

**To keep Colab online, press key F12 and put below codes on Websites Console, finally run it with Enter key.**

```
function ConnectButton(){
	console.log("Connect pushed");
	document.querySelector("#top-toolbar > colab-connect-button").shadowRoot.querySelector("#connect").click()
}
setInterval(ConnectButton,60000);
```
Freeze_batch_size can be set to 16, but Unfreeze_batch_size should be set less than 8.

Considering the limited GPU RAM, GPU cannot run successfully if not so.

![image](https://user-images.githubusercontent.com/86788385/209096783-08b8dc68-07f9-48fe-ac42-dd838bc6e436.png)

## Tips

While adding MHSA_Block into YOLOv7_L, i found that a lot of layers had been created.

But the pre_weights file `yolov7_weights.pth` cannot be load on these newborned layers.

I had verified my idea that the freeze layers should be set to zero which would help the result to be better.

**`Keep Learning`**

