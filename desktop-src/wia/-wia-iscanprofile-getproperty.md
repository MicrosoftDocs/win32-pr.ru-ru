---
description: Возвращает значение указанных дочерних свойств в элементе <Properties> элемент профиля сканирования.
ms.assetid: 528b51f5-51e0-4639-965d-ee318eb2187b
title: Метод Исканпрофиле::-Property (Сканпрофиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetProperty
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: ef09115c7131df21697540fa941f8bd863650bc029601088b4a0f8c80e9b1a44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814084"
---
# <a name="iscanprofilegetproperty-method"></a>Исканпрофиле:: метод Property

Возвращает значение указанных дочерних свойств в `<Properties>` элементе профиля сканирования.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetProperty(
  [in]  ULONG       num,
  [in]  PROPID      *pid,
  [out] PROPVARIANT *pvar
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

*ПВАР* \[ заполняет\]
</dt> <dd>

Тип: **[пропвариант](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)\***

Указатель на массив значений.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Возвращает \_ значение false, если какое-либо из значений свойств недоступно; в противном случае возвращает s \_ OK или стандартный код ошибки COM.

## <a name="remarks"></a>Remarks

Тип каждого значения должен быть того же типа, который был задан при вызове [**исканпрофиле:: SetProperty**](-wia-iscanprofile-setproperty.md).

Каждое значение в массиве, на которое указывает *PID* , является одной из [констант свойства WIA](-wia-wia-property-constants.md). Эту систему идентификации можно расширить. См. раздел [Определение пользовательских свойств](-wia-defining-custom-properties.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Заголовок<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
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

 

 
