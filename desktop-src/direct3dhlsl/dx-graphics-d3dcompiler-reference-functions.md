---
title: Функции компилятора (Справочник по HLSL)
description: В этом разделе содержатся сведения о следующих функциях компилятора Direct3D HLSL.
ms.assetid: aacc5207-3ec8-4031-b5c9-f7c0fb7b7095
keywords:
- функции, компилятор
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ee63fa17cc9216fdb92f69fed4d77bc65bb49048
ms.sourcegitcommit: 11f52354f570aacaf1ba2a266b2e507abd73352a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/19/2021
ms.locfileid: "104987410"
---
# <a name="compiler-functions-hlsl-reference"></a>Функции компилятора (Справочник по HLSL)

В этом разделе содержатся сведения о следующих функциях компилятора Direct3D HLSL:

## <a name="in-this-section"></a>В этом разделе



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Раздел</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br/></td>
<td>Возвращает указатель на интерфейс отражения.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br/></td>
<td>Скомпилируйте код HLSL или файл эффектов в байтах для заданного целевого объекта.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br/></td>
<td>Компилирует код языка шейдера уровня Microsoft (HLSL) в байтовую кодировку для заданного целевого объекта.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows. См &quot; . раздел компиляция шейдеров для UWP &quot; в примечаниях для <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.
</blockquote>
<br/> Компилирует код HLSL в байтовые коды для заданного целевого объекта.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.
</blockquote>
<br/> Сжимает набор шейдеров в более компактной форме. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br/></td>
<td>Создает буфер.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br/></td>
<td>Создает интерфейс взаимодействия между функциями и графами. <br/>
<blockquote>
[!Note]<br />
Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br/></td>
<td>Создает интерфейс компоновщика. <br/>
<blockquote>
[!Note]<br />
Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.
</blockquote>
<br/> Распаковывает один или несколько шейдеров из сжатого набора. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br/></td>
<td>Разборку скомпилированного кода HLSL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br/></td>
<td>Разборку скомпилированного кода HLSL из Direct3D10ного действия.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br/></td>
<td>Разкомпилирует раздел скомпилированного кода HLSL, который указан в шагах трассировки шейдера.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br/></td>
<td>Разборку определенной области скомпилированного кода HLSL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br/></td>
<td>Извлекает определенную часть из результата компиляции.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.
</blockquote>
<br/> Получает отладочную информацию шейдера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1. Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .
</blockquote>
<br/> Возвращает входные и выходные подписи из результата компиляции.<br/></td>
</tr>
<tr class="odd">
<td>[<strong>D3DGetInputSignatureBlob</strong>] (/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1. Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .
</blockquote>
<br/> Возвращает входную подпись из результата компиляции.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
<a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1. Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .
</blockquote>
<br/> Возвращает выходную подпись из результата компиляции.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br/></td>
<td>Возвращает смещение в байтах для инструкций в разделе кода шейдера.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br/></td>
<td>Создает интерфейс модуля шейдера из исходных данных для модуля шейдера. <br/>
<blockquote>
[!Note]<br />
Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br/></td>
<td>Предварительно обрабатывает некомпилированный код HLSL.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.
</blockquote>
<br/> Считывает файл, который находится на диске, в память.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br/></td>
<td>Возвращает указатель на интерфейс отражения.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br/></td>
<td>Создает интерфейс отражения библиотеки из исходных данных, который содержит HLSL библиотеку функций. <br/>
<blockquote>
[!Note]<br />
Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br/></td>
<td>Задает сведения в результате компиляции.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br/></td>
<td>Удаляет ненужные большие двоичные объекты из результата компиляции.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
Этот API можно использовать для разработки приложений для Магазина Windows, но его нельзя использовать в приложениях, отправляемых в магазин Windows.
</blockquote>
<br/> Записывает большой двоичный объект памяти в файл на диске.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Справочник по D3DCompiler](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

