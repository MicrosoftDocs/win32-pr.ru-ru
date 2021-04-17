---
title: Метод ФилеассоЦиатионс класса Win32_TSApplicationFileExtensions
description: Сканирует реестр для получения текущих сопоставлений файлов для приложения.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода ФилеассоЦиатионс
- Службы удаленных рабочих столов метода ФилеассоЦиатионс, класс Win32_TSApplicationFileExtensions
- Класс Win32_TSApplicationFileExtensions службы удаленных рабочих столов, метод ФилеассоЦиатионс
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105682088"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a>Метод ФилеассоЦиатионс \_ класса Win32 тсаппликатионфиликстенсионс

Сканирует реестр для получения текущих сопоставлений файлов для приложения.

## <a name="syntax"></a>Синтаксис


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Апппас* \[ окне\]
</dt> <dd>

Указывает путь к приложению.

</dd> <dt>

*ФилеассоЦиатионс* \[ заполняет\]
</dt> <dd>

При успешном завершении содержит сопоставления файлов для этого приложения.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тсаллов. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Тсаппликатионфиликстенсионс Win32**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**\_РдфилеассоЦиатион Win32**](win32-rdfileassociation.md)
</dt> </dl>

 

 





