---
description: Задает значение указанных дочерних свойств в элементе <Properties> элемент профиля сканирования.
ms.assetid: 3cf7b723-4004-49e5-b3bd-49a84432ede3
title: 'Метод Исканпрофиле:: SetProperty (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: ba4c7aff5139f1230179299d80065f1b933a6cf2d01d4ca03c045ccbe142c3cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118441430"
---
# <a name="iscanprofilesetproperty-method"></a>Метод Исканпрофиле:: SetProperty

Задает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetProperty(
  [in] ULONG       num,
  [in] PROPID      *pid,
  [in] PROPVARIANT *pvar
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*число* \[ окне\]
</dt> <dd>

Тип: **ulong**

Количество записей в массивах, на которые указывает *PID* и *ПВАР*.

</dd> <dt>

*идентификатор процесса* \[ окне\]
</dt> <dd>

Тип: **PropID \***

Указатель на массив идентификационных номеров заданных свойств. Каждое значение в массиве является [константами свойства WIA](-wia-wia-property-constants.md).

</dd> <dt>

*ПВАР* \[ окне\]
</dt> <dd>

Тип: **[пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Указатель на массив значений, присваиваемый свойствам.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="remarks"></a>Remarks

Каждое значение в массиве, на которое указывает *PID* , является одной из [констант свойства WIA](-wia-wia-property-constants.md). Эту систему идентификации можно расширить. См. раздел [Определение пользовательских свойств](-wia-defining-custom-properties.md).

Изменения в профиле не сохраняются на диск, пока приложение не вызовет метод [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) .

Если два приложения создают объекты профиля сканирования из одного и того же XML-файла и каждое приложение записывает изменения в свой объект, только изменения, внесенные приложением, которое вызывает [**исканпрофиле:: Save**](-wia-iscanprofile-save.md) Last, сохраняются на диске.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также

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

 

 
