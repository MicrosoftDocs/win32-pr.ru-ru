---
description: D3DXMath — это математическая вспомогательная библиотека для приложений Direct3D.
ms.assetid: 3067d47f-9b1d-2051-fa24-2094418ea272
title: Работа с D3DXMath
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d463129a453a2b319dd72790bd4546dd90f63a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898249"
---
# <a name="working-with-d3dxmath"></a>Работа с D3DXMath

D3DXMath — это математическая вспомогательная библиотека для приложений Direct3D. D3DXMath является долговременным, включается в D3DX 9 и D3DX 10, а также даты обратно в более старые версии DirectX.

> [!Note]  
> Библиотека служебной программы D3DX (D3DX 9, D3DX 10 и D3DX 11) является устаревшей для Windows 8, поэтому мы настоятельно рекомендуем перейти на Директксмас, а не использовать D3DXMath.

 

Директксмас использует те же функции в D3DXMath, а внутреннее D3DXMath включает ряд оптимизаций для конкретного процессора. Основное отличие заключается в том, что D3DXMath размещается в D3DX9 \* . DLL и D3DX10 \* . Библиотеки DLL и некоторые функции являются встроенными. Соглашение о вызовах библиотеки Директксмас явно понятно, тогда как D3DXMath должен выполнять операции Load и Store для реализации SIMD-оптимизации.

## <a name="mixing-directxmath-and-d3dxmath"></a>Смешивание Директксмас и D3DXMath

D3DX11 не содержит D3DXMath, и в целом мы рекомендуем использовать вместо него Директксмас. Тем не менее, вы можете продолжить связь с D3DX9 и (или) D3DX10 в приложении, поэтому вы можете продолжать использовать D3DXMath или одновременно в приложении одновременно использовать D3DXMath и Директксмас.

В общем случае можно выполнить приведение КСМВЕКТОР \* к функции, принимающей D3DXVECTOR4, \* или для приведения ксмматрикс \* к функции, принимающей D3DXMATRIX \* . Однако обратная кодировка не является надежной, так как КСМВЕКТОР и КСММАТРИКС должны быть сопоставлены 16 байт, тогда как D3DXVECTOR4 и D3DXMATRIX не имеют такого требования. Несоблюдение этого требования может привести к недопустимым исключениям выравнивания во время выполнения.

Можно выполнить приведение КСМВЕКТОР \* к функции, которая принимает D3DXVECTOR2 \* или D3DXVECTOR3 \* , но не наоборот. Как проблемы выравнивания, так и тот факт, что D3DXVECTOR2 и D3DXVECTOR3 являются более мелкими структурами, делают эту операцию ненадежной.

> [!Note]  
> D3DX (и, следовательно, D3DXMath) считается устаревшим и недоступен для приложений Магазина Windows, работающих в Windows 8 и не включенных в пакет SDK для Windows 8 для классических приложений.

 

## <a name="using-directxmath-with-direct3d"></a>Использование Директксмас с Direct3D

Директксмас и D3DXMath необязательны при работе с Direct3D. Direct3D 9 определил D3DMATRIX и D3DCOLOR как часть API Direct3D для поддержки конвейера фиксированной функции (теперь устаревшей версии). D3DXMath в D3DX9 расширяет эти типы Direct3D 9 с помощью общих математических операций с графикой. Для Direct3D 10. x и Direct3D 11 API-интерфейс использует только программируемый конвейер, поэтому нет специальной структуры API для матриц или значений цвета. Если для новых API требуется значение цвета, они принимают явный массив значений float или универсальный буфер постоянных данных, интерпретируемых шейдером HLSL. HLSL сам по себе может поддерживать форматы матрицы строк или основных столбцов, поэтому макет полностью подойдет вам (Дополнительные сведения см. в разделе HLSL, [упорядочение матрицы](../direct3dhlsl/dx-graphics-hlsl-per-component-math.md). Если в шейдере используются форматы столбцов крупной матрицы, то необходимо переставить данные матрицы директксмас при помещении их в структуры буферов констант). В то время как необязательно, библиотеки Директксмас и D3DXMath предоставляют общие функции, связанные с графикой, и поэтому чрезвычайно удобны при выполнении программирования Direct3D.

Можно легко привести КСМВЕКТОР \* к D3DVECTOR \* или КСММАТРИКС \* в D3DMATRIX, \* так как Direct3D 9 не делает никаких предположений относительно структуры входящих данных. Также можно выполнить приведение КСМКОЛОР к D3DCOLOR. Можно преобразовать представление Color с 4 плавающей запятой в КСМКОЛОР через Ксмстореколор (), чтобы получить 8:8:8:8 32-разрядный DWORD, эквивалентный D3DCOLOR.

При работе с Direct3D 10. x или Direct3D 11 обычно используются типы Директксмас для создания структуры для каждого буфера констант, и в таких случаях он в основном зависит от способности управлять выравниванием, чтобы сделать их эффективным, или использовать \* операции ксмсторе () для преобразования данных ксмвектор и ксмматрикс в правильные типы данных. При вызове интерфейсов API Direct3D 10. x или Direct3D 11, для которых требуется массив значений цвета с плавающей запятой \[ 4 \] , можно привести КСМВЕКТОР \* или XMFLOAT4, \* содержащий данные цвета.

## <a name="porting-from-d3dxmath"></a>Перенос из D3DXMath



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Тип D3DXMath</th>
<th>Эквивалент Директксмас</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>D3DXFLOAT16</td>
<td><a href="half-data-type.md"><strong>ПОЛТОР</strong></a></td>
</tr>
<tr class="even">
<td>D3DXMATRIX</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4x4"><strong>XMFLOAT4X4</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXMATRIXA16</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmmatrix"><strong>Ксмматрикс</strong></a> или <a href="/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)"> <strong>XMFLOAT4X4A</strong></a></td>
</tr>
<tr class="even">
<td>D3DXQUATERNION<br/> D3DXPLANE<br/> D3DXCOLOR<br/></td>
<td><a href="xmvector-data-type.md"><strong>Ксмвектор</strong></a> используется вместо уникальных типов, поэтому вам, скорее всего, потребуется использовать <a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"> <strong>XMFLOAT4</strong></a>
<blockquote>
[!Note]<br />
[<strong>D3DXQUATERNION:: operator *</strong>] (.. /Direct3D9/d3dxquaternion-Extensions.md) вызывает функцию <a href="/windows/desktop/direct3d9/d3dxquaternionmultiply"><strong>D3DXQuaternionMultiply</strong></a> , которая умножает два кватерниона. Но если вы явно не используете функцию <a href="/windows/desktop/api/directxmath/nf-directxmath-xmquaternionmultiply"><strong>ксмкуатернионмултипли</strong></a> , вы получаете неверный ответ при использовании <a href="xmvector-operator-mul.md"><strong>ксмвектор:: operator *</strong></a> для кватерниона.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR2</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat2"><strong>XMFLOAT2</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR2_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2"><strong>XMHALF2</strong></a></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR3</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat3"><strong>XMFLOAT3</strong></a></td>
</tr>
<tr class="even">
<td>D3DXVECTOR4</td>
<td><a href="/windows/desktop/api/directxmath/ns-directxmath-xmfloat4"><strong>XMFLOAT4</strong></a>(или, если вы можете гарантировать, что данные будут сопоставлены 16 байт, <a href="xmvector-data-type.md"><strong>ксмвектор</strong></a> или <a href="/previous-versions/windows/desktop/legacy/ee419609(v=vs.85)"><strong>XMFLOAT4A</strong></a> )<br/></td>
</tr>
<tr class="odd">
<td>D3DXVECTOR4_16F</td>
<td><a href="/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4"><strong>XMHALF4</strong></a></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> В Кснамас нет прямого эквивалента D3DXVECTOR3 \_ 16F.

 



| Макрос D3DXMath | Эквивалент Директксмас                            |
|----------------|---------------------------------------------------|
| D3DX \_ Pi       | [XM \_ Pi](ovw-xnamath-reference-constants.md)     |
| D3DX \_ 1BYPI    | [XM \_ 1DIVPI](ovw-xnamath-reference-constants.md) |
| D3DXToRadian   | [**ксмконвертторадианс**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttoradians)  |
| D3DXToDegree   | [**ксмконверттодегрис**](/windows/desktop/api/DirectXMath/nf-directxmath-xmconverttodegrees)  |



 



| Функция D3DXMath                  | Эквивалент Директксмас                                                                                                                                                                                                                           |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXBoxBoundProbe                  | [**BoundingBox:: intersects (КСМВЕКТОР, КСМВЕКТОР, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-intersects(fxmvector_fxmvector_float_))                                                                                                                                                          |
| D3DXComputeBoundingBox             | [**BoundingBox:: Креатефромпоинтс**](/windows/win32/api/directxcollision/nf-directxcollision-boundingbox-createfrompoints)                                                                                                                                                                          |
| D3DXComputeBoundingSphere          | [**Баундингсфере:: Креатефромпоинтс**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-createfrompoints)                                                                                                                                                                      |
| D3DXSphereBoundProbe               | [**Баундингсфере:: intersects (КСМВЕКТОР, КСМВЕКТОР, float&)**](/windows/win32/api/directxcollision/nf-directxcollision-boundingsphere-intersects(fxmvector_fxmvector_float_))                                                                                                                                                    |
| D3DXIntersectTriFunction           | [**Трианглетестс:: intersects**](ovw-xnamath-triangletests.md)                                                                                                                                                                                   |
| D3DXFloat32To16Array               | [**ксмконвертфлоаттохалфстреам**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconvertfloattohalfstream)                                                                                                                                                                                 |
| D3DXFloat16To32Array               | [**ксмконверсалфтофлоатстреам**](/windows/win32/api/directxpackedvector/nf-directxpackedvector-xmconverthalftofloatstream)                                                                                                                                                                                 |
| D3DXVec2Length                     | [**XMVector2Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector2length) или [ **XMVector2LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthest)                                                                                                                                                   |
| D3DXVec2LengthSq                   | [**XMVector2LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector2lengthsq)                                                                                                                                                                                                   |
| D3DXVec2Dot                        | [**XMVector2Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector2dot)                                                                                                                                                                                                             |
| D3DXVec2CCW                        | [**XMVector2Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector2cross)                                                                                                                                                                                                         |
| D3DXVec2Add                        | [**ксмвекторадд**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec2Subtract                   | [**ксмвекторсубтракт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec2Minimize                   | [**ксмвектормин**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec2Maximize                   | [**ксмвектормакс**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec2Scale                      | [**ксмвекторскале**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec2Lerp                       | [**Ксмвекторлерп**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) или [ **ксмвекторлерпв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec2Normalize                  | [**XMVector2Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalize) или [ **XMVector2NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector2normalizeest)                                                                                                                                       |
| D3DXVec2Hermite                    | [**Ксмвекторхермите**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) или [ **ксмвекторхермитев**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec2CatmullRom                 | [**Ксмвекторкатмуллром**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) или [ **ксмвекторкатмуллромв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec2BaryCentric                | [**Ксмвекторбарицентрик**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) или [ **ксмвекторбарицентрикв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec2Transform                  | [**XMVector2Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transform)                                                                                                                                                                                                 |
| D3DXVec2TransformCoord             | [**XMVector2TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoord)                                                                                                                                                                                       |
| D3DXVec2TransformNormal            | [**XMVector2TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormal)                                                                                                                                                                                     |
| D3DXVec2TransformArray             | [**XMVector2TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformstream)                                                                                                                                                                                     |
| D3DXVec2TransformCoordArray        | [**XMVector2TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformcoordstream)                                                                                                                                                                           |
| D3DXVec2TransformNormalArray       | [**XMVector2TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector2transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Length                     | [**XMVector3Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector3length) или [ **XMVector3LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthest)                                                                                                                                                   |
| D3DXVec3LengthSq                   | [**XMVector3LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector3lengthsq)                                                                                                                                                                                                   |
| D3DXVec3Dot                        | [**XMVector3Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector3dot)                                                                                                                                                                                                             |
| D3DXVec3Cross                      | [**XMVector3Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector3cross)                                                                                                                                                                                                         |
| D3DXVec3Add                        | [**ксмвекторадд**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec3Subtract                   | [**ксмвекторсубтракт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec3Minimize                   | [**ксмвектормин**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec3Maximize                   | [**ксмвектормакс**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec3Scale                      | [**ксмвекторскале**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec3Lerp                       | [**Ксмвекторлерп**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) или [ **ксмвекторлерпв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec3Normalize                  | [**XMVector3Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalize) или [ **XMVector3NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector3normalizeest)                                                                                                                                       |
| D3DXVec3Hermite                    | [**Ксмвекторхермите**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) или [ **ксмвекторхермитев**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec3CatmullRom                 | [**Ксмвекторкатмуллром**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) или [ **ксмвекторкатмуллромв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec3BaryCentric                | [**Ксмвекторбарицентрик**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) или [ **ксмвекторбарицентрикв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec3Transform                  | [**XMVector3Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transform)                                                                                                                                                                                                 |
| D3DXVec3TransformCoord             | [**XMVector3TransformCoord**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoord)                                                                                                                                                                                       |
| D3DXVec3TransformNormal            | [**XMVector3TransformNormal**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormal)                                                                                                                                                                                     |
| D3DXVec3TransformArray             | [**XMVector3TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformstream)                                                                                                                                                                                     |
| D3DXVec3TransformCoordArray        | [**XMVector3TransformCoordStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformcoordstream)                                                                                                                                                                           |
| D3DXVec3TransformNormalArray       | [**XMVector3TransformNormalStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3transformnormalstream)                                                                                                                                                                         |
| D3DXVec3Project                    | [**XMVector3Project**](/windows/win32/api/directxmath/nf-directxmath-xmvector3project)                                                                                                                                                                                                     |
| D3DXVec3Unproject                  | [**XMVector3Unproject**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unproject)                                                                                                                                                                                                 |
| D3DXVec3ProjectArray               | [**XMVector3ProjectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3projectstream)                                                                                                                                                                                         |
| D3DXVec3UnprojectArray             | [**XMVector3UnprojectStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector3unprojectstream)                                                                                                                                                                                     |
| D3DXVec4Length                     | [**XMVector4Length**](/windows/win32/api/directxmath/nf-directxmath-xmvector4length) или [ **XMVector4LengthEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthest)                                                                                                                                                   |
| D3DXVec4LengthSq                   | [**XMVector4LengthSq**](/windows/win32/api/directxmath/nf-directxmath-xmvector4lengthsq)                                                                                                                                                                                                   |
| D3DXVec4Dot                        | [**XMVector4Dot**](/windows/win32/api/directxmath/nf-directxmath-xmvector4dot)                                                                                                                                                                                                             |
| D3DXVec4Add                        | [**ксмвекторадд**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXVec4Subtract                   | [**ксмвекторсубтракт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXVec4Minimize                   | [**ксмвектормин**](/windows/win32/api/directxmath/nf-directxmath-xmvectormin)                                                                                                                                                                                                               |
| D3DXVec4Maximize                   | [**ксмвектормакс**](/windows/win32/api/directxmath/nf-directxmath-xmvectormax)                                                                                                                                                                                                               |
| D3DXVec4Scale                      | [**ксмвекторскале**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXVec4Lerp                       | [**Ксмвекторлерп**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) или [ **ксмвекторлерпв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXVec4Cross                      | [**XMVector4Cross**](/windows/win32/api/directxmath/nf-directxmath-xmvector4cross)                                                                                                                                                                                                         |
| D3DXVec4Normalize                  | [**XMVector4Normalize**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalize) или [ **XMVector4NormalizeEst**](/windows/win32/api/directxmath/nf-directxmath-xmvector4normalizeest)                                                                                                                                       |
| D3DXVec4Hermite                    | [**Ксмвекторхермите**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermite) или [ **ксмвекторхермитев**](/windows/win32/api/directxmath/nf-directxmath-xmvectorhermitev)                                                                                                                                                       |
| D3DXVec4CatmullRom                 | [**Ксмвекторкатмуллром**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullrom) или [ **ксмвекторкатмуллромв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorcatmullromv)                                                                                                                                           |
| D3DXVec4BaryCentric                | [**Ксмвекторбарицентрик**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentric) или [ **ксмвекторбарицентрикв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorbarycentricv)                                                                                                                                       |
| D3DXVec4Transform                  | [**XMVector4Transform**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transform)                                                                                                                                                                                                 |
| D3DXVec4TransformArray             | [**XMVector4TransformStream**](/windows/win32/api/directxmath/nf-directxmath-xmvector4transformstream)                                                                                                                                                                                     |
| D3DXMatrixIdentity                 | [**ксмматриксидентити**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixidentity)                                                                                                                                                                                                     |
| D3DXMatrixDeterminant              | [**ксмматриксдетерминант**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdeterminant)                                                                                                                                                                                               |
| D3DXMatrixDecompose                | [**ксмматриксдекомпосе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixdecompose)                                                                                                                                                                                                   |
| D3DXMatrixTranspose                | [**ксмматрикстранспосе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranspose)                                                                                                                                                                                                   |
| D3DXMatrixMultiply                 | [**ксмматриксмултипли**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiply)                                                                                                                                                                                                     |
| D3DXMatrixMultiplyTranspose        | [**ксмматриксмултиплитранспосе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixmultiplytranspose)                                                                                                                                                                                   |
| D3DXMatrixInverse                  | [**ксмматриксинверсе**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixinverse)                                                                                                                                                                                                       |
| D3DXMatrixScaling                  | [**ксмматриксскалинг**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixscaling)                                                                                                                                                                                                       |
| D3DXMatrixTranslation              | [**ксмматрикстранслатион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtranslation)                                                                                                                                                                                               |
| D3DXMatrixRotationX                | [**ксмматриксротатионкс**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationx)                                                                                                                                                                                                   |
| D3DXMatrixRotationY                | [**ксмматриксротатиони**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationy)                                                                                                                                                                                                   |
| D3DXMatrixRotationZ                | [**ксмматриксротатионз**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationz)                                                                                                                                                                                                   |
| D3DXMatrixRotationAxis             | [**ксмматриксротатионаксис**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationaxis)                                                                                                                                                                                             |
| D3DXMatrixRotationQuaternion       | [**ксмматриксротатионкуатернион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationquaternion)                                                                                                                                                                                 |
| D3DXMatrixRotationYawPitchRoll     | [**Ксмматриксротатионроллпитчяв**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixrotationrollpitchyaw) (Обратите внимание, что порядок параметров отличается: D3DXMatrixRotationYawPitchRoll принимает значения нутации, шаг, рулон, **ксмматриксротатионроллпитчяв** — шаг, значения нутации, рулон).                 |
| D3DXMatrixTransformation           | [**ксмматрикстрансформатион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation)                                                                                                                                                                                         |
| D3DXMatrixTransformation2D         | [**XMMatrixTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixtransformation2d)                                                                                                                                                                                     |
| D3DXMatrixAffineTransformation     | [**ксмматриксаффинетрансформатион**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation)                                                                                                                                                                             |
| D3DXMatrixAffineTransformation2D   | [**XMMatrixAffineTransformation2D**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixaffinetransformation2d)                                                                                                                                                                         |
| D3DXMatrixLookAtRH                 | [**XMMatrixLookAtRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatrh)                                                                                                                                                                                                     |
| D3DXMatrixLookAtLH                 | [**XMMatrixLookAtLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixlookatlh)                                                                                                                                                                                                     |
| D3DXMatrixPerspectiveRH            | [**XMMatrixPerspectiveRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiverh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveLH            | [**XMMatrixPerspectiveLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivelh)                                                                                                                                                                                           |
| D3DXMatrixPerspectiveFovRH         | [**XMMatrixPerspectiveFovRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovrh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveFovLH         | [**XMMatrixPerspectiveFovLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectivefovlh)                                                                                                                                                                                     |
| D3DXMatrixPerspectiveOffCenterRH   | [**XMMatrixPerspectiveOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterrh)                                                                                                                                                                         |
| D3DXMatrixPerspectiveOffCenterLH   | [**XMMatrixPerspectiveOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixperspectiveoffcenterlh)                                                                                                                                                                         |
| D3DXMatrixOrthoRH                  | [**XMMatrixOrthographicRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicrh)                                                                                                                                                                                         |
| D3DXMatrixOrthoLH                  | [**XMMatrixOrthographicLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographiclh)                                                                                                                                                                                         |
| D3DXMatrixOrthoOffCenterRH         | [**XMMatrixOrthographicOffCenterRH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterrh)                                                                                                                                                                       |
| D3DXMatrixOrthoOffCenterLH         | [**XMMatrixOrthographicOffCenterLH**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixorthographicoffcenterlh)                                                                                                                                                                       |
| D3DXMatrixShadow                   | [**ксмматриксшадов**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixshadow)                                                                                                                                                                                                         |
| D3DXMatrixReflect                  | [**ксмматриксрефлект**](/windows/win32/api/directxmath/nf-directxmath-xmmatrixreflect)                                                                                                                                                                                                       |
| D3DXQuaternionLength               | [**ксмкуатернионленгс**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlength)                                                                                                                                                                                                 |
| D3DXQuaternionLengthSq             | [**ксмкуатернионленгсск**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionlengthsq)                                                                                                                                                                                             |
| D3DXQuaternionDot                  | [**ксмкуатерниондот**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniondot)                                                                                                                                                                                                       |
| D3DXQuaternionIdentity             | [**ксмкуатернионидентити**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionidentity)                                                                                                                                                                                             |
| D3DXQuaternionIsIdentity           | [**ксмкуатернионисидентити**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionisidentity)                                                                                                                                                                                         |
| D3DXQuaternionConjugate            | [**ксмкуатернионконжугате**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionconjugate)                                                                                                                                                                                           |
| D3DXQuaternionToAxisAngle          | [**ксмкуатернионтоаксисангле**](/windows/win32/api/directxmath/nf-directxmath-xmquaterniontoaxisangle)                                                                                                                                                                                       |
| D3DXQuaternionRotationMatrix       | [**ксмкуатернионротатионматрикс**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationmatrix)                                                                                                                                                                                 |
| D3DXQuaternionRotationAxis         | [**ксмкуатернионротатионаксис**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationaxis)                                                                                                                                                                                     |
| D3DXQuaternionRotationYawPitchRoll | [**Ксмкуатернионротатионроллпитчяв**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionrotationrollpitchyaw) (Обратите внимание, что порядок параметров отличается: D3DXQuaternionRotationYawPitchRoll принимает значения нутации, шаг, рулон, **ксмкуатернионротатионроллпитчяв** — шаг, значения нутации, рулон). |
| D3DXQuaternionMultiply             | [**ксмкуатернионмултипли**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionmultiply)                                                                                                                                                                                             |
| D3DXQuaternionNormalize            | [**Ксмкуатернионнормализе**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalize) или [ **ксмкуатернионнормализист**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionnormalizeest)                                                                                                                           |
| D3DXQuaternionInverse              | [**ксмкуатернионинверсе**](/windows/win32/api/directxmath/nf-directxmath-xmquaternioninverse)                                                                                                                                                                                               |
| D3DXQuaternionLn                   | [**ксмкуатернионлн**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionln)                                                                                                                                                                                                         |
| D3DXQuaternionExp                  | [**ксмкуатернионексп**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionexp)                                                                                                                                                                                                       |
| D3DXQuaternionSlerp                | [**Ксмкуатернионслерп**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerp) или [ **ксмкуатернионслерпв**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionslerpv)                                                                                                                                               |
| D3DXQuaternionSquad                | [**Ксмкуатернионскуад**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquad) или [ **ксмкуатернионскуадв**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadv)                                                                                                                                               |
| D3DXQuaternionSquadSetup           | [**ксмкуатернионскуадсетуп**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionsquadsetup)                                                                                                                                                                                         |
| D3DXQuaternionBaryCentric          | [**Ксмкуатернионбарицентрик**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentric) или [ **ксмкуатернионбарицентрикв**](/windows/win32/api/directxmath/nf-directxmath-xmquaternionbarycentricv)                                                                                                                       |
| D3DXPlaneDot                       | [**ксмпланедот**](/windows/win32/api/directxmath/nf-directxmath-xmplanedot)                                                                                                                                                                                                                 |
| D3DXPlaneDotCoord                  | [**ксмпланедоткурд**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotcoord)                                                                                                                                                                                                       |
| D3DXPlaneDotNormal                 | [**ксмпланедотнормал**](/windows/win32/api/directxmath/nf-directxmath-xmplanedotnormal)                                                                                                                                                                                                     |
| D3DXPlaneScale                     | [**ксмвекторскале**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXPlaneNormalize                 | [**Ксмпланенормализе**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalize) или [ **ксмпланенормализист**](/windows/win32/api/directxmath/nf-directxmath-xmplanenormalizeest)                                                                                                                                               |
| D3DXPlaneIntersectLine             | [**ксмпланеинтерсектлине**](/windows/win32/api/directxmath/nf-directxmath-xmplaneintersectline)                                                                                                                                                                                             |
| D3DXPlaneFromPointNormal           | [**ксмпланефромпоинтнормал**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompointnormal)                                                                                                                                                                                         |
| D3DXPlaneFromPoints                | [**ксмпланефромпоинтс**](/windows/win32/api/directxmath/nf-directxmath-xmplanefrompoints)                                                                                                                                                                                                   |
| D3DXPlaneTransform                 | [**ксмпланетрансформ**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransform)                                                                                                                                                                                                     |
| D3DXPlaneTransformArray            | [**ксмпланетрансформстреам**](/windows/win32/api/directxmath/nf-directxmath-xmplanetransformstream)                                                                                                                                                                                         |
| D3DXColorNegative                  | [**ксмколорнегативе**](/windows/win32/api/directxmath/nf-directxmath-xmcolornegative)                                                                                                                                                                                                       |
| D3DXColorAdd                       | [**ксмвекторадд**](/windows/win32/api/directxmath/nf-directxmath-xmvectoradd)                                                                                                                                                                                                               |
| D3DXColorSubtract                  | [**ксмвекторсубтракт**](/windows/win32/api/directxmath/nf-directxmath-xmvectorsubtract)                                                                                                                                                                                                     |
| D3DXColorScale                     | [**ксмвекторскале**](/windows/win32/api/directxmath/nf-directxmath-xmvectorscale)                                                                                                                                                                                                           |
| D3DXColorModulate                  | [**ксмколормодулате**](/windows/win32/api/directxmath/nf-directxmath-xmcolormodulate)                                                                                                                                                                                                       |
| D3DXColorLerp                      | [**Ксмвекторлерп**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerp) или [ **ксмвекторлерпв**](/windows/win32/api/directxmath/nf-directxmath-xmvectorlerpv)                                                                                                                                                                   |
| D3DXColorAdjustSaturation          | [**ксмколораджустсатуратион**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustsaturation)                                                                                                                                                                                       |
| D3DXColorAdjustContrast            | [**ксмколораджустконтраст**](/windows/win32/api/directxmath/nf-directxmath-xmcoloradjustcontrast)                                                                                                                                                                                           |
| D3DXFresnelTerm                    | [**ксмфреснелтерм**](/windows/win32/api/directxmath/nf-directxmath-xmfresnelterm)                                                                                                                                                                                                           |



 

> [!Note]  
> Функции [сферического гармонического](https://github.com/Microsoft/DirectXMath/tree/master/SHMath) директксмас доступны отдельно. Директксмас не имеет эквивалента **ID3DXMatrixStack**.

 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Директксмас по программированию](ovw-xnamath-progguide.md)
</dt> </dl>

 

 
