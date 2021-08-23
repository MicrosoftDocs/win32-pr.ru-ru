---
description: Параметры — это переменные эффектов.
ms.assetid: vs|directx_sdk|~\parameters.htm
title: Параметры (Direct3D 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc28d1410180aac54daf306fe586694cfa1b7f4123403efc606a77385d088326
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606684"
---
# <a name="parameters-direct3d-9"></a>Параметры (Direct3D 9)

Параметры — это переменные эффектов.

## <a name="syntax"></a>Синтаксис

*идентификатор типа использования* \[ : *выражение семантических* \] \[ < *заметок* > \] \[ =   \] ;

Параметры можно считывать из приложения и записывать в него с помощью [**ID3DXEffect**](id3dxeffect.md) или [**ID3DXEffectCompiler**](id3dxeffectcompiler.md).

На параметры можно ссылаться в функциях и в методах (в частности, в правой части назначений состояний).



| Элемент                                                                                 | Описание                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="usage"></span><span id="USAGE"></span>*Загрузка*<br/>                   | Область действия параметра. См. раздел [использование и литералы (Direct3D 9)](usages-and-literals.md).<br/>                                                             |
| <span id="type"></span><span id="TYPE"></span>*Тип*<br/>                      | Любая допустимая [ссылка для типа HLSL](../direct3dhlsl/dx-graphics-hlsl-reference.md) .<br/>                                                                        |
| <span id="ID"></span><span id="id"></span>*УДОСТОВЕРЕНИЯ*<br/>                            | Уникальное имя.<br/>                                                                                                                                       |
| <span id="semantic"></span><span id="SEMANTIC"></span>*семантическ*<br/>          | Тег, следующий за правилами идентификаторов, который обычно указывает на использование параметра. Должен быть определенным типом.<br/>                                     |
| <span id="annotations"></span><span id="ANNOTATIONS"></span>*Примечания*<br/> | Ноль или более частей пользовательской информации. Может быть любым типом. См. раздел [Добавление сведений, чтобы параметры вступили в действие с заметками](using-an-effect.md).<br/> |
| <span id="expression"></span><span id="EXPRESSION"></span>*выражение*<br/>    | Инициализирует значение параметра. См. раздел [выражения (Direct3D 9)](expressions.md).<br/>                                                                  |



 

Параметры могут быть инициализированы любой допустимой [ссылкой](../direct3dhlsl/dx-graphics-hlsl-reference.md) на выражение HLSL, которое сокращается до литерального значения.

Значения параметров не изменяются при выполнении назначения состояния или вызовах функций.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Формат эффектов](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
