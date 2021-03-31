---
description: Удаляет указанный список дочерних свойств в элементе <Properties> элемент профиля сканирования.
ms.assetid: 512ccfec-0c95-4abb-98b6-d309e432151b
title: 'Метод Исканпрофиле:: RemoveProperty (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.RemoveProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 1ac1d713ab36da5c35ea7a0d7c523699e7c85b34
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154871"
---
# <a name="iscanprofileremoveproperty-method"></a>Метод Исканпрофиле:: RemoveProperty

Удаляет указанный список дочерних свойств `<Properties>` элемента профиля сканирования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RemoveProperty(
  [in] ULONG  num,
  [in] PROPID *pid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*число* \[ окне\]
</dt> <dd>

Тип: **ulong**

Количество записей в массиве, на которое указывает *PID* .

</dd> <dt>

*идентификатор процесса* \[ окне\]
</dt> <dd>

Тип: **PropID \** _

Указатель на массив идентификационных номеров удаляемых свойств. Каждая из них является [константами свойства WIA](-wia-wia-property-constants.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: _ *HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Комментарии

Каждое значение в массиве, на которое указывает *PID* , является одной из [констант свойства WIA](-wia-wia-property-constants.md). Эту систему идентификации можно расширить. См. раздел [Определение пользовательских свойств](-wia-defining-custom-properties.md).

Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .

Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ классических приложений Windows Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

**Зрения**
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> <dt>

[Константы свойств WIA](-wia-wia-property-constants.md)
</dt> <dt>

[Определение пользовательских свойств](-wia-defining-custom-properties.md)
</dt> </dl>

 

 




