---
title: Метод Сетклиентакцесснаме класса Win32_RDMSEnvironment
description: Обновляет имя записи ресурса службы доменных имен (DNS) в среде служб управления удаленный рабочий стол (RDMS).
ms.assetid: bbce3fc1-d2c5-4874-bdd0-be27fb5981d1
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Сетклиентакцесснаме
- Службы удаленных рабочих столов метода Сетклиентакцесснаме, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Сетклиентакцесснаме
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.SetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: efbb962a6dd1600ad0cd439f7f34772f69d91b925308e2247e1283575d8f68cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118604876"
---
# <a name="setclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Метод Сетклиентакцесснаме \_ класса Win32 рдмсенвиронмент

Обновляет имя записи ресурса службы доменных имен (DNS) в среде служб управления удаленный рабочий стол (RDMS).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetClientAccessName(
  [in] string ClientAccessName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Клиентакцесснаме* \[ окне\]
</dt> <dd>

Новое имя записи ресурса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсенвиронмент Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





