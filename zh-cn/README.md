# 概要

<div class="align-center">

## 下载地址
着色器: [BOOTH](https://lilxyzw.booth.pm/items/3087170) / [GitHub](https://github.com/lilxyzw/lilToon/releases) / [VRChat Creator Companion](vcc://vpm/addRepo?url=https://lilxyzw.github.io/vpm-repos/vpm.json)  
ロゴ: [GitHub](https://github.com/lilxyzw/lilToon/tree/master/logo)

## 特性
这是一个为使用头像的服务开发的着色器，具有以下特性。

</div>

<div class="flexwrapcontainer">
<div class="flex2">
<h3>简单</h3>
<p>支持从预设进行一键设置，保存自定义预设。一旦你创建了一个材质，下次就可以一键设置。此外，还配备了用于头像修改的色彩校正功能，你创建的颜色可以导出为纹理。</p>
</div>

<div class="flex2">
<h3>美观</h3>
<p>我们深入研究了插图的绘制，并在着色器上装备了可以表达的各种功能。通过抗锯齿着色，也可以平滑地再现动漫绘制。此外，考虑到VRSNS的情况，我们采取了防止彻底白色飞溅和通过半透明物体如水防止透明度的措施。</p>
</div>

<div class="flex2">
<h3>轻量</h3>
<p>编辑器会自动重写着色器以打开和关闭功能，并排除不必要的功能以最小化负载。此外，我们也努力最小化构建大小，因此你可以在VRSNS中减少头像容量。</p>
</div>

<div class="flex2">
<h3>稳定</h3>
<p>目前已经兼容所有Unity照明系统，并接近Standard Shader的亮度。此外，它支持广泛的Unity版本，以便在各种环境中长期使用，减少着色器迁移的麻烦。（Unity2017 - 2021，BRP/LWRP/URP/HDRP）</p>
</div>
</div>

<div class="bg-black">
<div class="align-center">

## 兼容性
为了能在各种环境中长期使用，它支持广泛的Unity版本。

</div>
<div class="flexcontainer">
    <div class="flex3">
        <h3>Unity版本</h3>
        <ul>
            <li>2018.1 - 2018.4</li>
            <li>2019.1 - 2019.4</li>
            <li>2020.1 - 2020.3</li>
            <li>2021.1 - 2021.3</li>
            <li>2022.1 - 2022.3</li>
            <li>2023.1 - 2023.2</li>
        </ul>
    </div>
    <div class="flex3">
        <h3>着色器模型</h3>
        <ul>
            <li>通常版: SM4.0・ES3.0</li>
            <li>轻量版: SM3.0・ES2.0</li>
            <li>毛皮: SM4.0・ES3.1+AEP・ES3.2</li>
            <li>细分: SM5.0・ES3.1+AEP・ES3.2</li>
        </ul>
    </div>
    <div class="flex3">
        <h3>渲染管线</h3>
        <ul>
            <li>内建渲染管线</li>
            <li>轻量渲染管线</li>
            <li>通用渲染管线</li>
            <li>高清渲染管线</li>
        </ul>
    </div>
</div>

<div class="small-container">

※ 经过测试的兼容环境如下：
- Unity 2018.1.0f2 (Built-in RP)
- Unity 2018.4.20f1 (Built-in RP / LWRP 4.10.0 / HDRP 4.10.0)
- Unity 2019.2.21f1 (Built-in RP / LWRP 6.9.2 / HDRP 6.9.2)
- Unity 2019.3.0f6 (Built-in RP / URP 7.1.8 / HDRP 7.1.8)
- Unity 2019.4.31f1 (Built-in RP / URP 7.7.1 / HDRP 7.7.1)
- Unity 2020.3.47f1 (Built-in RP / URP 10.10.1 / HDRP 10.10.1)
- Unity 2021.3.23f1 (Built-in RP / URP 12.1.11 / HDRP 12.1.11)
- Unity 2022.3.15f1 (Built-in RP / URP 14.0.8 / HDRP 14.0.8)
- Unity 2023.2.0a11 (Built-in RP / URP 16.0.1 / HDRP 16.0.1)

</div>
</div>

## 主要功能
- [UV滚动&旋转](/zh-cn/base/uv.md) - 可以进行平铺或动画处理，或者在多边形的正反两面使用不同的UV，等等各种变化。
- [主色](/zh-cn/color/maincolor.md) - 考虑到角色改造，支持通过色彩校正进行色彩更换和纹理输出。
- [主色2nd/3rd](/zh-cn/color/maincolor_layer.md) - 支持贴花、细节、层次遮罩、Gif动画、距离淡出，以及各种合成模式。
- [Alpha遮罩](/zh-cn/color/alphamask.md) - 也可以将其烧录到主纹理的Alpha通道并输出。
- [三重阴影](/zh-cn/color/shadow.md) - 可以通过纹理指定颜色，指定阴影边界的颜色，通过AO遮罩调整阴影的易附性。
- [发光x2](/zh-cn/color/emission.md) - 支持动画、遮罩、闪烁、颜色的时间变化、视差，可以进行多样化的表现。
- [法线贴图x2](/zh-cn/reflections/normal.md) - 可以单独调整UV和强度，第一张图可以调整大致的阴影方向，第二张图可以添加细节。
- [各向异性反射](/zh-cn/reflections/anisotropy.md) - 可以应用于反射和MatCap。可以表现出如头发或发线完成等复杂的质感。
- [逆光](/zh-cn/reflections/backlight.md) - 可以表现出常在插图中使用的从后方照射的光。
- [镜面反射](/zh-cn/reflections/reflection.md) - 可以表现出从插图风格的高光到照片真实的反射。由于支持CubeMap的fallback和override，因此也可以进行不受环境影响的表现。
- [MatCap x2](/zh-cn/reflections/matcap.md) - 支持Z轴旋转取消、透视校正、UV1混合的Angel Ring表现，以及各种合成模式。
- [边缘光](/zh-cn/reflections/rimlight.md) - 可以根据光源方向调整阳光部分和阴影部分的颜色、模糊量和范围。
- [闪光](/zh-cn/reflections/glitter.md) - 可以表现出像闪光一样复杂的光泽质感。
- [宝石](/zh-cn/reflections/gem.md) - 可以表现出通常的着色器难以表现的宝石的闪烁质感。
- [轮廓线](/zh-cn/advanced/outline.md) - 支持纹理颜色指定、遮罩、距离相关的粗细校正。此外，即使在硬边模型上，也可以使用顶点颜色进行平滑绘制。
- [视差贴图](/zh-cn/advanced/parallax.md) - 可以通过根据视线方向移动UV来伪造立体感。
- [距离淡出](/zh-cn/advanced/distancefade.md) - 可以通过在接近时变暗来增加现场感，或者反转淡出效果以用作雾。
- [AudioLink](/zh-cn/advanced/audiolink.md) - 在支持的VRChat世界中，可以根据音频同步动画材质。
- [Dissolve](/zh-cn/advanced?id=dissolve.md) - 可以用于出现和退出动画、变形效果、部分溶解表现等各种用途。
- [AvatarEncryption](/zh-cn/advanced/encryption.md) - 使用四个密钥对网格进行加密，以防止模型被盗取。
- [曲面细分](/zh-cn/advanced/tessellation.md) - 当靠近时使模型更加平滑，主要用于视频制作。
- [折射](/zh-cn/advanced/refraction.md) - 可以实现类似玻璃的折射效果。
- [毛皮](/zh-cn/advanced/fur.md) - 可以表现出类似毛发的复杂质感。
- 距离裁剪消除器 - 即使靠得很近也不会消失，特别适用于VR等场景。可以通过在着色器设置中开启此功能。
- [针对VRChat的功能](/zh-cn/base/vrchat.md) - 这是一个当着色器失效时用于指定备用着色器的功能。

## 许可证
本着色器以[MIT License](https://github.com/lilxyzw/lilToon/blob/master/Assets/lilToon/LICENSE)发布。你可以在[这里](https://licenses.opensource.jp/MIT/MIT.html)查看日语参考译文。关于第三方许可证，请查看[Third Party Notices.md](https://github.com/lilxyzw/lilToon/blob/master/Assets/lilToon/Third%20Party%20Notices.md)。