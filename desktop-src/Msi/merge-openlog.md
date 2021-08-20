---
description: Метод Опенлог объекта Merge открывает файл журнала, который получает сведения о ходе выполнения и сообщениях об ошибках. Если файл журнала уже существует, установщик добавляет новые сообщения. Если файл журнала не существует, установщик создает файл журнала.
ms.assetid: 97d01ea3-43b6-4529-9706-97b3b0132d9c
title: Метод Merge. Опенлог (Мержемод. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Merge.OpenLog
- IMsmMerge.OpenLog
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: c69ecf0c7a4a629b2f6ebc303d34619ae9d4cc396c79e09ea37e2d4b27db5c3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117804616"
---
# <a name="mergeopenlog-method"></a>Метод Merge. Опенлог

Метод **опенлог** объекта [**Merge**](merge-object.md) открывает файл журнала, который получает сведения о ходе выполнения и сообщениях об ошибках. Если файл журнала уже существует, установщик добавляет новые сообщения. Если файл журнала не существует, установщик создает файл журнала.

## <a name="syntax"></a>Синтаксис


```JScript
Merge.OpenLog(
  Filename
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя файла* 
</dt> <dd>

Полное имя файла, указывающее на файл, который нужно открыть или создать.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="remarks"></a>Remarks

Клиенты могут отправить свои сообщения в этот файл журнала с помощью метода [**log**](merge-log.md) .

### <a name="c"></a>C++

См. раздел Функция [**опенлог**](/windows/win32/api/mergemod/nf-mergemod-imsmmerge-openlog) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|-----------------------------------------------------------------------------------------|
| Версия<br/> | Mergemod.dll 1,0 или более поздней версии<br/>                                                    |
| Заголовок<br/>  | <dl> <dt>Мержемод. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 
