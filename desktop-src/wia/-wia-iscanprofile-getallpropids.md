---
description: Возвращает все доступные идентификаторы свойств в профиле.
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'Метод Исканпрофиле:: Жеталлпропидс (Сканпрофиле. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 7fd54e3e1cd45c3631df9b069ddf3c2e897037efb2870d00946f0a002e12f145
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118965783"
---
# <a name="iscanprofilegetallpropids-method"></a>Метод Исканпрофиле:: Жеталлпропидс

Возвращает все доступные идентификаторы свойств в профиле.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*число* \[ в, out\]
</dt> <dd>

Тип: **ulong \***

Количество запрошенных или возвращаемых идентификаторов свойств.

</dd> <dt>

*PPID* \[ заполняет\]
</dt> <dd>

Тип: **PropID \***

Указатель на массив идентификаторов свойств.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **HRESULT**

Если этот метод завершается успешно, возвращается значение **S \_ ОК**. В противном случае возвращается код ошибки **HRESULT** .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows \[Только классические приложения Vista\]<br/>                                              |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2008\]<br/>                                        |
| Header<br/>                   | <dl> <dt>Сканпрофиле. h</dt> </dl>    |
| IDL<br/>                      | <dl> <dt>Сканпрофилес. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**исканпрофиле**](-wia-iscanprofile.md)
</dt> <dt>

[Схема профиля сканирования](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




