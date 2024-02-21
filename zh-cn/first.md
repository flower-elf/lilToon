# 开始

## 出现的术语
这些是在Unity等3DCG处理中会出现的术语。理解这些可以帮助你更容易理解手册和你正在寻找的功能。

|名称|描述|
|-|-|
|材质|决定物体外观的数据。|
|纹理|就是图片。用于决定物体的颜色等，有各种用途。|
|UV|决定纹理贴图位置的数据。|
|遮罩|用于指定进行处理的部分的纹理。|
|法线贴图|使表面看起来有凹凸的纹理。影响阴影和光泽的表现。|
|MatCap|描绘了光反射的纹理。|
|边缘光|像逆光一样，光线环绕物体，只有物体的轮廓会变亮。|
|模板|屏幕上进行的遮罩表现。例如，可以在头发上绘制眉毛等表现。|

## 导入步骤和简单使用方法

<div class="timeline">
<div class="timeline_part">
    <div class="timeline_label">步骤 1</div>
    <div class="timeline_title">下载着色器</div>
    <div class="timeline_text">你可以从<a href="https://lilxyzw.booth.pm/items/3087170">BOOTH</a>或<a href="https://github.com/lilxyzw/lilToon/releases">GitHub</a>下载。有几种变体，但请只导入适合你需求的相应版本。
    <div class="window_info">&#x1f530; 如果你要在VRChat中使用，也可以<a href="vcc://vpm/addRepo?url=https://lilxyzw.github.io/vpm-repos/vpm.json">点击这里</a>添加到VCC。添加到VCC后，它会显示在 Manage Project 的包列表中，你可以按下+按钮或手动选择包版本来添加。<span>如果是从VCC添加，就不需要进行步骤 2 的unitypackage导入步骤了</span>。</div>

|类型|用途|
|-|-|
|无标记|这是用于Built-in RP的。如果你要在VRChat中使用，请使用这个。BOOTH可下载的文件只包含这个变体。|
|LWRP|这是用于Lightweight Render Pipeline（LWRP）的。它是URP的旧版本，现在几乎不再使用，但由于支持成本几乎为零，所以我们保留了它。我们可能会在将来删除对它的支持。|
|URP|这是用于Universal Render Pipeline（URP）的。|
|HDRP|这是用于High Definition Render Pipeline（HDRP）的。|

</div>
</div>

<div class="timeline_part">
    <div class="timeline_label">步骤 2</div>
    <div class="timeline_title">导入unitypackage</div>
    <div class="timeline_text">接下来，请将你刚刚下载的扩展名为「<span>.unitypackage</span>」的文件拖放到Unity的<span>项目窗口</span>中。也可以使用<a href="https://docs.unity3d.com/ja/current/Manual/upm-ui-giturl.html" target="_blank" rel="noopener noreferrer">Unity Package Manager</a>，但是更新可能会比较困难，所以如果你是为了VRChat，使用unitypackage或VCC可能更稳妥。
        <div class="window_info">&#x1f530; <span>如果你已经有设置好的模型数据，那么步骤 3 以后的操作就不需要了</span>。步骤 3 以后的操作是为了新建模型或进行着色器迁移。</div>
    </div>
</div>
<div class="timeline_part timeline_part_sub">
    <div class="timeline_label">步骤 3</div>
    <div class="timeline_title">创建材质</div>
    <div class="timeline_text">选择材质，然后在Inspector的顶部将"Shader"更改为"lilToon"。<span>"_lil"中的着色器是特殊的，所以基本上应该选择普通的"lilToon"</span>。另外，如果没有材质，你可以手动创建新的，或者在FBX的导入设置中选择Materials选项卡，然后<a href="https://docs.unity3d.com/ja/current/Manual/FBXImporter-Materials.html" target="_blank" rel="noopener noreferrer">更改导入设置</a>。</div>
</div>
<div class="timeline_part timeline_part_sub">
    <div class="timeline_label">步骤 4</div>
    <div class="timeline_title">更改编辑模式</div>
    <div class="timeline_text">接下来，请将<a href="#">编辑模式</a>更改为<span>详细设置</span>。简单设置是为了<span>只想更改已经设置好的模型颜色的初学者</span>，详细设置是为了<span>新建设置或迁移着色器，或者想进行详细修改的中级和高级用户</span>。
        <div class="window_info">&#x26a0; 在某些环境中，可能默认不是日语显示。在这种情况下，请将Language更改为<span>Japanese</span>。</div>
    </div>
</div>
<div class="timeline_part timeline_part_sub">
    <div class="timeline_label">步骤 5</div>
    <div class="timeline_title">分配纹理</div>
    <div class="timeline_text">如果没有分配纹理，那么请在基本颜色设置中的<span>主颜色</span>指定纹理。如果有其他类型的纹理，如法线贴图等，那么请按照下表在相应的位置分配。

|类型|分配位置|
|-|-|
|主纹理|基本颜色设置 > 主颜色 > 纹理|
|法线贴图|法线贴图设置 > 法线贴图 > 法线贴图|
|轮廓线遮罩|轮廓线设置 > 轮廓线 > 遮罩和宽度|
|阴影遮罩|阴影设置 > 阴影 > 遮罩和强度|
|MatCap|MatCap设置 > MatCap > MatCap|
|MatCap遮罩|MatCap设置 > MatCap > 遮罩|
|边缘光遮罩|边缘光设置 > 边缘光 > 颜色 / 遮罩|
|发光（遮罩）|发光设置 > 发光纹理 > 颜色|

</div>
</div>
<div class="timeline_part timeline_part_sub">
    <div class="timeline_label">步骤 6</div>
    <div class="timeline_title">更改渲染模式</div>
    <div class="timeline_text">如果需要使纹理透明，那么请将"Rendering Mode（透明模式）"更改为<span>剪切</span>或<span>半透明</span>。</div>
</div>
<div class="timeline_part timeline_part_sub">
    <div class="timeline_label">步骤 7</div>
    <div class="timeline_title">应用预设</div>
    <div class="timeline_text">你可以更改<a href="#">编辑模式</a>为预设，然后应用适合你目标的预设来简单地进行设置。以上就是基本的使用方法。如果你想进行更详细的编辑，请查看各功能的手册。</div>
</div>
</div>
## lilToonを用いた制作物の配布について
- シェーダーを同梱する場合は、[BOOTH](https://booth.pm/ja/items/3087170)や[GitHub](https://github.com/lilxyzw/lilToon/releases)のダウンロードページへのショートカットを同梱する方法か、ダウンロードしてきたそのままのシェーダーのunitypackageを同梱する方法がオススメです
- シェーダー本体と制作物を1つのunitypackageにまとめる方法は、ユーザーがインポート時に古いバージョンで上書きしてしまう問題が発生する可能性があるため非推奨です

## ロゴデータ
ロゴデータは[こちら](https://github.com/lilxyzw/lilToon/tree/master/logo)からダウンロードできます。  
BOOTH等の販売サイトでのサムネイルへの使用や作品への使用・同梱が可能で、商品ページでのライセンスの記載も不要です。  
色や解像度を変更し、作品にマッチしたイメージに変更することもできます。

## シェーダーバリエーション
パッケージに含まれるシェーダーのバリエーションの一覧です。

|名前|説明|
|-|-|
|lilToon|メインのシェーダーです。一般的な用途ではこれを使用します。|
|_lil/[Optional] lilToonOverlay|マテリアルの上に重ねて表示するための透過シェーダーです。不要なパスが除去されており、通常の透過シェーダーを重ねるより低負荷です。|
|_lil/[Optional] lilToonOutlineOnly|輪郭線のみのシェーダーです。例えば、ハードエッジのモデルで輪郭線を描画する場合に別途法線がスムーズなメッシュを用意してこのシェーダーを割り当てることにより、通常より綺麗な輪郭線を描画できます。|
|_lil/[Optional] lilToonFurOnly|ファーの毛の部分のみを描画するシェーダーです。通常のシェーダーに重ねる表現や、カットアウトのファーと透過のファーを組み合わせた表現をする場合にオススメです。|
|_lil/lilToonMulti|シェーダーキーワードを利用するバージョンです。マテリアルを大量に使用する場合などにビルドサイズが大きくなりやすいため注意が必要です。|
|Hidden/lilToonLite|通常版の見た目をある程度維持しつつ大幅に軽量化したものです。Lite版から直接マテリアルを設定せず、通常版で作成したものを変換するとより直感的にマテリアル設定が可能です。|