---
description: Свойство Модулефилес объекта GetObject возвращает все первичные ключи таблицы файлов для текущего открытого модуля.
ms.assetid: e1c8049c-b271-4def-abde-89ea99393574
title: Свойство файла. Модулефилес (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles.ModuleFiles
- IMsmGetFiles.get_ModuleFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: b4b7d498979c94de048e72058df4c8bf87fb8607220efe808554d66deb5d89ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635944"
---
# <a name="getfilesmodulefiles-property"></a>Файл Модулефилес.

Свойство **модулефилес** [**объекта GetObject возвращает**](getfiles-object.md) все первичные ключи [таблицы файлов](file-table.md) для текущего открытого модуля. Первичные ключи возвращаются в виде коллекции строк. Модуль должен быть открыт путем вызова метода [**опенмодуле**](merge-openmodule.md) [объекта Merge](merge-object.md) перед вызовом **модулефилес**.

Это свойство доступно только для чтения.

## <a name="syntax"></a>Синтаксис


```JScript
propVal = GetFiles.ModuleFiles
```



## <a name="property-value"></a>Значение свойства

## <a name="remarks"></a>Remarks

Обратите внимание, что порядок файлов, перечисленных в коллекции, может не находиться в той же последовательности, которая указана в таблице File.

Если модуль не имеет таблицы файлов или не содержит файлов на определенном языке, Модулефилес возвращает пустую коллекцию строк.

### <a name="c"></a>C++

См. раздел [**Получение функции \_ модулефилес**](/windows/win32/api/mergemod/nf-mergemod-imsmgetfiles-get_modulefiles) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Header<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
