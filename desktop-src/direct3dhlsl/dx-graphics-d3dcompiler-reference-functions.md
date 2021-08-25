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
ms.openlocfilehash: 43d9bf2feb572d7b410d702dbc456af7c18be0ee
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465811"
---
# <a name="compiler-functions-hlsl-reference"></a>Функции компилятора (Справочник по HLSL)

В этом разделе содержатся сведения о следующих функциях компилятора Direct3D HLSL:

## <a name="in-this-section"></a>В этом разделе




| Раздел | Описание | 
|-------|-------------|
| <a href="d3d11reflect.md"><strong>D3D11Reflect</strong></a><br /> | Возвращает указатель на интерфейс отражения.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile"><strong>D3DCompile</strong></a><br /> | Скомпилируйте код HLSL или файл эффектов в байтах для заданного целевого объекта.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a><br /> | Компилирует код языка шейдера уровня Microsoft (HLSL) в байтовую кодировку для заданного целевого объекта.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile"><strong>D3DCompileFromFile</strong></a><br /> | <blockquote>[!Note]<br />этот API можно использовать для разработки приложений магазина Windows, но его нельзя использовать в приложениях, отправляемых в хранилище Windows. См. раздел "компиляция шейдеров для UWP" в примечаниях для <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2"><strong>D3DCompile2</strong></a>.</blockquote><br /> Компилирует код HLSL в байтовые коды для заданного целевого объекта.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompressshaders"><strong>D3DCompressShaders</strong></a><br /> | <blockquote>[!Note]<br />этот API можно использовать для разработки приложений магазина Windows, но его нельзя использовать в приложениях, отправляемых в хранилище Windows.</blockquote><br /> Сжимает набор шейдеров в более компактной форме. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcreateblob"><strong>D3DCreateBlob</strong></a><br /> | Создает буфер.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph"><strong>D3DCreateFunctionLinkingGraph</strong></a><br /> | Создает интерфейс взаимодействия между функциями и графами. <br /><blockquote>[!Note]<br />Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dcreatelinker"><strong>D3DCreateLinker</strong></a><br /> | Создает интерфейс компоновщика. <br /><blockquote>[!Note]<br />Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddecompressshaders"><strong>D3DDecompressShaders</strong></a><br /> | <blockquote>[!Note]<br />этот API можно использовать для разработки приложений магазина Windows, но его нельзя использовать в приложениях, отправляемых в хранилище Windows.</blockquote><br /> Распаковывает один или несколько шейдеров из сжатого набора. <br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble"><strong>D3DDisassemble</strong></a><br /> | Разборку скомпилированного кода HLSL.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect"><strong>D3DDisassemble10Effect</strong></a><br /> | Разборку скомпилированного кода HLSL из Direct3D10ного действия.<br /> | 
| <a href="/windows/win32/api/d3d11shadertracing/nf-d3d11shadertracing-d3ddisassemble11trace"><strong>D3DDisassemble11Trace</strong></a><br /> | Разкомпилирует раздел скомпилированного кода HLSL, который указан в шагах трассировки шейдера.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassembleregion"><strong>D3DDisassembleRegion</strong></a><br /> | Разборку определенной области скомпилированного кода HLSL.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a><br /> | Извлекает определенную часть из результата компиляции.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetdebuginfo"><strong>D3DGetDebugInfo</strong></a><br /> | <blockquote>[!Note]<br />этот API можно использовать для разработки приложений магазина Windows, но его нельзя использовать в приложениях, отправляемых в хранилище Windows.</blockquote><br /> Получает отладочную информацию шейдера.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputandoutputsignatureblob"><strong>D3DGetInputAndOutputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1. Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_AND_OUTPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Возвращает входные и выходные подписи из результата компиляции.<br /> | 
| [<strong>D3DGetInputSignatureBlob</strong>](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob)<br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetinputsignatureblob"><strong>D3DGetInputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1. Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_INPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Возвращает входную подпись из результата компиляции.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a><br /> | <blockquote>[!Note]<br /><a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetoutputsignatureblob"><strong>D3DGetOutputSignatureBlob</strong></a> может быть изменен или недоступен для выпусков после Windows 8.1. Вместо этого используйте <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgetblobpart"><strong>D3DGetBlobPart</strong></a> со значением <a href="/windows/win32/api/d3dcompiler/ne-d3dcompiler-d3d_blob_part"><strong>D3D_BLOB_OUTPUT_SIGNATURE_BLOB</strong></a> .</blockquote><br /> Возвращает выходную подпись из результата компиляции.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dgettraceinstructionoffsets"><strong>D3DGetTraceInstructionOffsets</strong></a><br /> | Возвращает смещение в байтах для инструкций в разделе кода шейдера.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dloadmodule"><strong>D3DLoadModule</strong></a><br /> | Создает интерфейс модуля шейдера из исходных данных для модуля шейдера. <br /><blockquote>[!Note]<br />Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dpreprocess"><strong>D3DPreprocess</strong></a><br /> | Предварительно обрабатывает некомпилированный код HLSL.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreadfiletoblob"><strong>D3DReadFileToBlob</strong></a><br /> | <blockquote>[!Note]<br />этот API можно использовать для разработки приложений магазина Windows, но его нельзя использовать в приложениях, отправляемых в хранилище Windows.</blockquote><br /> Считывает файл, который находится на диске, в память.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dreflect"><strong>D3DReflect</strong></a><br /> | Возвращает указатель на интерфейс отражения.<br /> | 
| <a href="/windows/desktop/api/D3Dcompiler/nf-d3dcompiler-d3dreflectlibrary"><strong>D3DReflectLibrary</strong></a><br /> | Создает интерфейс отражения библиотеки из исходных данных, который содержит HLSL библиотеку функций. <br /><blockquote>[!Note]<br />Эта функция является частью технологии связывания шейдеров HLSL, которую можно использовать на всех платформах Direct3D 11 для создания предкомпилированных функций HLSL, их упаковки в библиотеки и связывания их с полными шейдерами во время выполнения.</blockquote><br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dsetblobpart"><strong>D3DSetBlobPart</strong></a><br /> | Задает сведения в результате компиляции.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dstripshader"><strong>D3DStripShader</strong></a><br /> | Удаляет ненужные большие двоичные объекты из результата компиляции.<br /> | 
| <a href="/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dwriteblobtofile"><strong>D3DWriteBlobToFile</strong></a><br /> | <blockquote>[!Note]<br />этот API можно использовать для разработки приложений магазина Windows, но его нельзя использовать в приложениях, отправляемых в хранилище Windows.</blockquote><br /> Записывает большой двоичный объект памяти в файл на диске.<br /> | 




 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по D3DCompiler](dx-graphics-d3dcompiler-reference.md)
</dt> </dl>

