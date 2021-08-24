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
ms.openlocfilehash: a45548d055d6adc90ac55e26b646abab80470297847d5daa898e63b29769dc4d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119737514"
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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMv2 \\ терминалсервицес<br/>                                                |
| MOF<br/>                      | <dl> <dt>Тсаллов. mof</dt> </dl>  |
| DLL<br/>                      | <dl> <dt>TsPubWmi.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Тсаппликатионфиликстенсионс Win32**](win32-tsapplicationfileextensions.md)
</dt> <dt>

[**\_РдфилеассоЦиатион Win32**](win32-rdfileassociation.md)
</dt> </dl>

 

 





