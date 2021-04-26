---
description: Параметры для сохранения и создания эффектов.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995081"
---
# <a name="d3dxfx"></a>D3DXFX

Параметры для сохранения и создания эффектов.

Константы в следующей таблице определены в d3dx9effect. h.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Флаги сохранения и восстановления состояния эффектов</td>
<td>Описание</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESTATE</td>
<td>Состояние не сохраняется при вызове <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> или Restored при вызове <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_DONOTSAVESAMPLERSTATE</td>
<td>Статеблокк сохраняет состояние при вызове <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> и восстанавливает состояние при вызове <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DXFX_DONOTSAVESHADERSTATE</td>
<td>Статеблокк сохраняет состояние (за исключением шейдеров и констант шейдера) при вызове метода <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> и восстанавливает состояние при вызове <a href="id3dxeffect--end.md"><strong>End</strong></a>.</td>
</tr>
<tr class="odd">
<td>Флаги создания эффектов</td>
<td>Описание</td>
</tr>
<tr class="even">
<td>D3DXFX_NOT_CLONEABLE</td>
<td>Результат будет не клонирован и не будет содержать двоичные данные шейдера. <a href="id3dxbaseeffect--getpassdesc.md"><strong>Жетпассдеск</strong></a> не будет возвращать указатели функций шейдера. Установка этого флага сокращает использование памяти на 50%, так как устраняет необходимость сохранения копии шейдеров в памяти системой влияния. Этот флаг используется <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>и <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</td>
</tr>
<tr class="odd">
<td>D3DXFX_LARGEADDRESSAWARE</td>
<td>Разрешает выделение ресурса влияния в адресном пространстве уппдер компьютера. Одно важное ограничение заключается в том, что нельзя использовать строки и обрабатывать взаимозаменяемые. Например, следующее перестанет работать. <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

Вместо этого метод, такой как [<strong>жетпараметербинаме</strong>](id3dxbaseeffect--getparameterbyname.md) , должен использоваться для хранения маркера параметра, который затем используется для передачи переменных в результат.</td>
</tr>
</tbody>
</table>



 

Константы в следующей таблице не определены по умолчанию и должны определяться разработчиком.



| Определение препроцессора эффектов \# | Описание                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D3DXFX \_ ларжеаддресс \_   | Определите это значение перед включением d3dx9. h, чтобы приложение не было скомпилировано при попытке передать строки в параметры D3DXHANDLE. Это поможет убедиться в том, что в среду выполнения передаются допустимые данные. |
| Флаги компоновщика эффектов            | Описание                                                                                                                                                                                                                          |
| с \_ \_ учетом большого адреса          | Установка флага компоновщика "большой \_ адрес \_ " с учетом значения 1 позволит приложению распределять ресурсы за пределы 2 ГБ при необходимости.                                                                                      |



 

Система эффектов использует блоки состояний для автоматического сохранения и восстановления состояния. Дополнительные сведения о блоках состояния см. в разделе [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Константы эффектов](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



