---
title: 10Level9 ссылку ID3D11DeviceContext методы
description: В этом разделе перечислены различия между каждым уровнем функций 10Level9 и уровнем D3D \_ уровня \_ \_ 11 \_ 0 и более высоким уровнем функций для методов ссылку ID3D11DeviceContext.
ms.assetid: 84478b56-0306-491a-9545-0849b06d8342
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d5cb055e6a290a9500f65ad2d64cdd69b0eaa224e6a81359595688ba1aca657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118990074"
---
# <a name="10level9-id3d11devicecontext-methods"></a>10Level9 ссылку ID3D11DeviceContext методы

В этом разделе перечислены различия между каждым уровнем функций 10Level9 и уровнем D3D \_ уровня \_ \_ 11 \_ 0 и более высоким уровнем функций для методов [**ссылку ID3D11DeviceContext**](/windows/desktop/api/D3D11/nn-d3d11-id3d11devicecontext) .

-   [Ссылку ID3D11DeviceContext:: Кописубресаурцерегион](#id3d11devicecontextcopysubresourceregion)
-   [Ссылку ID3D11DeviceContext:: Копиресаурце](#id3d11devicecontextcopyresource)
-   [Ссылку ID3D11DeviceContext:: Копиструктурекаунт](#id3d11devicecontextcopystructurecount)
-   [Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевфлоат](#id3d11devicecontextclearunorderedaccessviewfloat)
-   [Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевуинт](#id3d11devicecontextclearunorderedaccessviewuint)
-   [Ссылку ID3D11DeviceContext:: Клеаррендертаржетвиев](#id3d11devicecontextclearrendertargetview)
-   [Ссылку ID3D11DeviceContext:: Кссетконстантбуфферс](#id3d11devicecontextcssetconstantbuffers)
-   [Ссылку ID3D11DeviceContext:: Кссетсамплерс](#id3d11devicecontextcssetsamplers)
-   [Ссылку ID3D11DeviceContext:: Кссетшадер](#id3d11devicecontextcssetshader)
-   [Ссылку ID3D11DeviceContext:: Кссетшадерресаурцес](#id3d11devicecontextcssetshaderresources)
-   [Ссылку ID3D11DeviceContext:: Кссетунордередакцессвиевс](#id3d11devicecontextcssetunorderedaccessviews)
-   [Ссылку ID3D11DeviceContext::D Patch](#id3d11devicecontextdispatch)
-   [Ссылку ID3D11DeviceContext::D Испатчиндирект](#id3d11devicecontextdispatchindirect)
-   [ID3D11DeviceContext::Draw](#id3d11devicecontextdraw)
-   [ID3D11DeviceContext::DrawAuto](#id3d11devicecontextdrawauto)
-   [ID3D11DeviceContext::DrawIndexed](#id3d11devicecontextdrawindexed)
-   [ID3D11DeviceContext::DrawIndexedInstanced](#id3d11devicecontextdrawindexedinstanced)
-   [Ссылку ID3D11DeviceContext::D Равиндексединстанцединдирект](#id3d11devicecontextdrawindexedinstancedindirect)
-   [ID3D11DeviceContext::DrawInstanced](#id3d11devicecontextdrawinstanced)
-   [Ссылку ID3D11DeviceContext::D Равинстанцединдирект](#id3d11devicecontextdrawinstancedindirect)
-   [Ссылку ID3D11DeviceContext::D Ссетконстантбуфферс](#id3d11devicecontextdssetconstantbuffers)
-   [Ссылку ID3D11DeviceContext::D Ссетсамплерс](#id3d11devicecontextdssetsamplers)
-   [Ссылку ID3D11DeviceContext::D Ссетшадер](#id3d11devicecontextdssetshader)
-   [Ссылку ID3D11DeviceContext::D Ссетшадерресаурцес](#id3d11devicecontextdssetshaderresources)
-   [Ссылку ID3D11DeviceContext:: Гссетконстантбуфферс](#id3d11devicecontextgssetconstantbuffers)
-   [Ссылку ID3D11DeviceContext:: Гссетсамплерс](#id3d11devicecontextgssetsamplers)
-   [Ссылку ID3D11DeviceContext:: Гссетшадер](#id3d11devicecontextgssetshader)
-   [Ссылку ID3D11DeviceContext:: Гссетшадерресаурцес](#id3d11devicecontextgssetshaderresources)
-   [Ссылку ID3D11DeviceContext:: Хссетконстантбуфферс](#id3d11devicecontexthssetconstantbuffers)
-   [Ссылку ID3D11DeviceContext:: Хссетсамплерс](#id3d11devicecontexthssetsamplers)
-   [Ссылку ID3D11DeviceContext:: Хссетшадер](#id3d11devicecontexthssetshader)
-   [Ссылку ID3D11DeviceContext:: Хссетшадерресаурцес](#id3d11devicecontexthssetshaderresources)
-   [ID3D11DeviceContext::IASetIndexBuffer](#id3d11devicecontextiasetindexbuffer)
-   [ID3D11DeviceContext::IASetPrimitiveTopology](#id3d11devicecontextiasetprimitivetopology)
-   [Ссылку ID3D11DeviceContext:: Омсетблендстате](#id3d11devicecontextomsetblendstate)
-   [Ссылку ID3D11DeviceContext:: Омсетрендертаржетс](#id3d11devicecontextomsetrendertargets)
-   [Ссылку ID3D11DeviceContext:: Омсетрендертаржетсандунордередакцессвиевс](#id3d11devicecontextomsetrendertargetsandunorderedaccessviews)
-   [Ссылку ID3D11DeviceContext::P Ссетконстантбуфферс](#id3d11devicecontextpssetconstantbuffers)
-   [Ссылку ID3D11DeviceContext::P Ссетсамплерс](#id3d11devicecontextpssetsamplers)
-   [Ссылку ID3D11DeviceContext::P Ссетшадер](#id3d11devicecontextpssetshader)
-   [Ссылку ID3D11DeviceContext::P Ссетшадерресаурцес](#id3d11devicecontextpssetshaderresources)
-   [Ссылку ID3D11DeviceContext:: РссетсЦиссорректс](#id3d11devicecontextrssetscissorrects)
-   [Ссылку ID3D11DeviceContext:: Рссетвиевпортс](#id3d11devicecontextrssetviewports)
-   [Ссылку ID3D11DeviceContext:: Сетпредикатион](#id3d11devicecontextsetpredication)
-   [Ссылку ID3D11DeviceContext:: Сосеттаржетс](#id3d11devicecontextsosettargets)
-   [Ссылку ID3D11DeviceContext:: Вссетконстантбуфферс](#id3d11devicecontextvssetconstantbuffers)
-   [Ссылку ID3D11DeviceContext:: Вссетсамплерс](#id3d11devicecontextvssetsamplers)
-   [Ссылку ID3D11DeviceContext:: Вссетшадер](#id3d11devicecontextvssetshader)
-   [Ссылку ID3D11DeviceContext:: Вссетшадерресаурцес](#id3d11devicecontextvssetshaderresources)
-   [Связанные темы](#related-topics)

## <a name="id3d11devicecontextcopysubresourceregion"></a>Ссылку ID3D11DeviceContext:: Кописубресаурцерегион



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> В памяти, доступной для GPU, могут копироваться только Texture2D и буферы.<br/> Texture3D не может быть скопирован из памяти, доступной GPU, в память, доступную для ЦП.<br/> Любой ресурс, имеющий только D3D10_BIND_SHADER_RESOURCE, не может быть скопирован из памяти, доступной на GPU, в память, доступную для ЦП.<br/> Копировать текстуры тома мипмаппед нельзя. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopyresource"></a>Ссылку ID3D11DeviceContext:: Копиресаурце



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3"> В памяти, доступной для GPU, могут копироваться только Texture2D и буферы.<br/> Texture3D не может быть скопирован из памяти, доступной GPU, в память, доступную для ЦП.<br/> Любой ресурс, имеющий только D3D10_BIND_SHADER_RESOURCE, не может быть скопирован из памяти, доступной на GPU, в память, доступную для ЦП.<br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcopystructurecount"></a>Ссылку ID3D11DeviceContext:: Копиструктурекаунт



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewfloat"></a>Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевфлоат



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearunorderedaccessviewuint"></a>Ссылку ID3D11DeviceContext:: Клеарунордередакцессвиевуинт



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextclearrendertargetview"></a>Ссылку ID3D11DeviceContext:: Клеаррендертаржетвиев



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Будет сброшен только первый срез массива. Приложения должны создать представление целевого объекта отрисовки для каждой грани или среза массива, а затем очистить каждое представление по отдельности. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetconstantbuffers"></a>Ссылку ID3D11DeviceContext:: Кссетконстантбуфферс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetsamplers"></a>Ссылку ID3D11DeviceContext:: Кссетсамплерс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshader"></a>Ссылку ID3D11DeviceContext:: Кссетшадер



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetshaderresources"></a>Ссылку ID3D11DeviceContext:: Кссетшадерресаурцес



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextcssetunorderedaccessviews"></a>Ссылку ID3D11DeviceContext:: Кссетунордередакцессвиевс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatch"></a>Ссылку ID3D11DeviceContext::D Patch



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdispatchindirect"></a>Ссылку ID3D11DeviceContext::D Испатчиндирект



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdraw"></a>ID3D11DeviceContext::Draw



| Уровень компонентов             | Различия в поведении                                                                                                               |
|---------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ уровень возможностей \_ 9 \_ 1 | Число примитивов не может превышать 65535.<br/> Текстуры не могут повторяться поверх одного примитива более 128 раз.<br/>    |
| D3D \_ \_ уровень возможностей \_ 9 \_ 2 | Число примитивов не может превышать 1048575.<br/> Текстуры не могут повторяться поверх одного примитива более 2048 раз.<br/> |
| D3D \_ \_ уровень возможностей \_ 9 \_ 3 | Число примитивов не может превышать 1048575.<br/> Текстуры не могут повторяться поверх одного примитива более 8192 раз.<br/> |



 

## <a name="id3d11devicecontextdrawauto"></a>ID3D11DeviceContext::DrawAuto



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexed"></a>ID3D11DeviceContext::DrawIndexed



| Уровень компонентов             | Различия в поведении                                                                                                                                                                                                            |
|---------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3D \_ \_ уровень возможностей \_ 9 \_ 1 | Число примитивов не может превышать 65535.<br/> Текстуры не могут повторяться поверх одного примитива более 128 раз.<br/> Значения индекса не могут превышать 65534.<br/> Списки индексированных точек не поддерживаются.<br/>      |
| D3D \_ \_ уровень возможностей \_ 9 \_ 2 | Число примитивов не может превышать 1048575.<br/> Текстуры не могут повторяться поверх одного примитива более 2048 раз.<br/> Значения индекса не могут превышать 1048575.<br/> Списки индексированных точек не поддерживаются.<br/> |
| D3D \_ \_ уровень возможностей \_ 9 \_ 3 | Число примитивов не может превышать 1048575.<br/> Текстуры не могут повторяться поверх одного примитива более 8192 раз.<br/> Значения индекса не могут превышать 1048575.<br/> Списки индексированных точек не поддерживаются.<br/> |



 

## <a name="id3d11devicecontextdrawindexedinstanced"></a>ID3D11DeviceContext::DrawIndexedInstanced



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Не поддерживается $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Число примитивов не может превышать 1048575.<br/> Текстуры не могут повторяться поверх одного примитива более 8192 раз.<br/> Значения индекса не могут превышать 1048575.<br/>
<blockquote>
[!Note]<br />
При вызове метода <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-drawindexedinstanced"><strong>дравиндексединстанцед</strong></a> с шейдером вершин, привязанным к конвейеру и не импортируя данные каждого экземпляра, некоторые графические аппаратные устройства с Direct3D 9 могут не рисовать ничего. В частности, если шейдер вершин не использует данные каждого экземпляра, вызов <strong>дравиндексединстанцед</strong> с 1 экземпляром не эквивалентен вызову <a href="/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-draw"><strong>Draw</strong></a>.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawindexedinstancedindirect"></a>Ссылку ID3D11DeviceContext::D Равиндексединстанцединдирект



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstanced"></a>ID3D11DeviceContext::DrawInstanced



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdrawinstancedindirect"></a>Ссылку ID3D11DeviceContext::D Равинстанцединдирект



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetconstantbuffers"></a>Ссылку ID3D11DeviceContext::D Ссетконстантбуфферс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetsamplers"></a>Ссылку ID3D11DeviceContext::D Ссетсамплерс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshader"></a>Ссылку ID3D11DeviceContext::D Ссетшадер



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextdssetshaderresources"></a>Ссылку ID3D11DeviceContext::D Ссетшадерресаурцес



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetconstantbuffers"></a>Ссылку ID3D11DeviceContext:: Гссетконстантбуфферс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetsamplers"></a>Ссылку ID3D11DeviceContext:: Гссетсамплерс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshader"></a>Ссылку ID3D11DeviceContext:: Гссетшадер



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextgssetshaderresources"></a>Ссылку ID3D11DeviceContext:: Гссетшадерресаурцес



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetconstantbuffers"></a>Ссылку ID3D11DeviceContext:: Хссетконстантбуфферс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetsamplers"></a>Ссылку ID3D11DeviceContext:: Хссетсамплерс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshader"></a>Ссылку ID3D11DeviceContext:: Хссетшадер



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontexthssetshaderresources"></a>Ссылку ID3D11DeviceContext:: Хссетшадерресаурцес



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="5">Не поддерживается на уровне функций 9. * или 10. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_10_0</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_10_1</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetindexbuffer"></a>ID3D11DeviceContext::IASetIndexBuffer



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td>Формат может отличаться от формата, указанного при создании буфера, но будет дорогостоящим переводом.<br/> Разрешает только буферы индексов с форматом DXGI_FORMAT_R16_UINT. <br/></td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>
<td rowspan="2"> Формат может отличаться от формата, указанного при создании буфера, но будет дорогостоящим переводом.<br/> Разрешает буферы индексов с форматами DXGI_FORMAT_R16_UINT и DXGI_FORMAT_R32_UINT, такими как D3D_FEATURE_LEVEL_10_0 и выше. <br/> $ {REMOVE} $<br />
</td>
</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextiasetprimitivetopology"></a>ID3D11DeviceContext::IASetPrimitiveTopology



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Примитивные топологии с соседями не поддерживаются $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetblendstate"></a>Ссылку ID3D11DeviceContext:: Омсетблендстате



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Самплемаск не может быть нулевым $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargets"></a>Ссылку ID3D11DeviceContext:: Омсетрендертаржетс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Поддерживается только один целевой объект прорисовки $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Поддерживаются только четыре целевого объекта отрисовки, и все связанные ресурсы должны иметь одинаковую глубину.</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextomsetrendertargetsandunorderedaccessviews"></a>Ссылку ID3D11DeviceContext:: Омсетрендертаржетсандунордередакцессвиевс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetconstantbuffers"></a>Ссылку ID3D11DeviceContext::P Ссетконстантбуфферс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">См. раздел уровень компонентов 10,0, но общее число констант, используемых шейдером, не может превышать 32 $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetsamplers"></a>Ссылку ID3D11DeviceContext::P Ссетсамплерс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Можно привязать не более 16 пробных выдолженстей $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshader"></a>Ссылку ID3D11DeviceContext::P Ссетшадер



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Только ps_4_0_level_9_1 $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Только ps_4_0_level_9_3 или ps_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextpssetshaderresources"></a>Ссылку ID3D11DeviceContext::P Ссетшадерресаурцес



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не более 8 одновременно привязанных ресурсов шейдера $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetscissorrects"></a>Ссылку ID3D11DeviceContext:: РссетсЦиссорректс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Доступен только начальном-прямоугольный прямоугольник $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextrssetviewports"></a>Ссылку ID3D11DeviceContext:: Рссетвиевпортс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Доступно только окно просмотра начальном $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

Даже если вы указали значения float для элементов структуры [**\_ окна просмотра D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) для массива *Пвиевпортс* в вызове [**ссылку ID3D11DeviceContext:: рссетвиевпортс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) для [уровней компонентов](overviews-direct3d-11-devices-downlevel-intro.md) 9 \_ x, **рссетвиевпортс** использует DWORD внутри. Из-за такого поведения при использовании отрицательного верхнего левого угла для окна просмотра, вызов **рссетвиевпортс** для уровней компонентов 9 \_ x завершается ошибкой. Эта ошибка возникает из-за того, что **рссетвиевпортс** для 9 \_ x приводит значения с плавающей запятой к целым числам без знака, не выполняя проверку, что приводит к переполнению целого числа.

Вызов [**ссылку ID3D11DeviceContext:: рссетвиевпортс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports) для [уровней компонентов](overviews-direct3d-11-devices-downlevel-intro.md) 10 \_ x и 11 \_ x работает так, как вы ожидаете, даже если для окна просмотра используется отрицательный верхний левый угол.

## <a name="id3d11devicecontextsetpredication"></a>Ссылку ID3D11DeviceContext:: Сетпредикатион



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextsosettargets"></a>Ссылку ID3D11DeviceContext:: Сосеттаржетс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetconstantbuffers"></a>Ссылку ID3D11DeviceContext:: Вссетконстантбуфферс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">См. раздел уровень компонентов 10,0, но общее число констант, используемых шейдером, не может превышать 255 $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetsamplers"></a>Ссылку ID3D11DeviceContext:: Вссетсамплерс



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshader"></a>Ссылку ID3D11DeviceContext:: Вссетшадер



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="2">Только vs_4_0_level_9_1 $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>
<td>Только vs_4_0_level_9_3 или vs_4_0_level_9_1</td>
</tr>
</tbody>
</table>



 

## <a name="id3d11devicecontextvssetshaderresources"></a>Ссылку ID3D11DeviceContext:: Вссетшадерресаурцес



<table>
<thead>
<tr class="header">
<th>Уровень компонентов</th>
<th>Различия в поведении</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_1</td>
<td rowspan="3">Не поддерживается на уровне функций 9. *. $ {Remove} $<br />
</td>
</tr>
<tr class="even">
<td>D3D_FEATURE_LEVEL_9_2</td>

</tr>
<tr class="odd">
<td>D3D_FEATURE_LEVEL_9_3</td>

</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по 10Level9](d3d11-graphics-reference-10level9.md)
</dt> </dl>

 

 





