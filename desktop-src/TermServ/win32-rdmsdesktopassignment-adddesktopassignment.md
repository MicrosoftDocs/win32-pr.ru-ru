---
title: Метод Адддесктопассигнмент класса Win32_RDMSDesktopAssignment
description: Добавьте назначение рабочего стола.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Адддесктопассигнмент
- Службы удаленных рабочих столов метода Адддесктопассигнмент, класс Win32_RDMSDesktopAssignment
- Класс Win32_RDMSDesktopAssignment службы удаленных рабочих столов, метод Адддесктопассигнмент
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0d8145318cfd749772d2dcf417b71c6a1862ee31ec363957554e06b3aa6257
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119868224"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Метод Адддесктопассигнмент \_ класса Win32 рдмсдесктопассигнмент

Добавление назначения рабочего стола

## <a name="syntax"></a>Синтаксис


```mof
uint32 AddDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Коллектионалиас* \[ окне\]
</dt> <dd>

Псевдоним коллекции.

</dd> <dt>

*Десктопнаме* \[ окне\]
</dt> <dd>

Имя рабочего стола.

</dd> <dt>

*Доменпользователя* \[ окне\]
</dt> <dd>

Доменное имя учетной записи пользователя.

</dd> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Имя учетной записи пользователя.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMV2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Рдмсдесктопассигнмент Win32**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





