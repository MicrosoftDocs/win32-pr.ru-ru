---
title: Метод Жетклиентакцесснаме класса Win32_RDMSEnvironment
description: Извлекает имя записи ресурса службы доменных имен (DNS) для среды управления удаленный рабочий стол (RDMS).
ms.assetid: 16f9d00d-a398-4a73-a641-ac552ba6a9d3
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Жетклиентакцесснаме
- Службы удаленных рабочих столов метода Жетклиентакцесснаме, класс Win32_RDMSEnvironment
- Класс Win32_RDMSEnvironment службы удаленных рабочих столов, метод Жетклиентакцесснаме
topic_type:
- apiref
api_name:
- Win32_RDMSEnvironment.GetClientAccessName
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 206ef89765bd18a73559c98d70a614664d076099214bd20f7b97ca9c29e94bc3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119139007"
---
# <a name="getclientaccessname-method-of-the-win32_rdmsenvironment-class"></a>Метод Жетклиентакцесснаме \_ класса Win32 рдмсенвиронмент

Извлекает имя записи ресурса службы доменных имен (DNS) для среды управления удаленный рабочий стол (RDMS).

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetClientAccessName(
  [out] string ClientAccessName
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Клиентакцесснаме* \[ заполняет\]
</dt> <dd>

Получает полученное имя записи ресурса.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Рдмсенвиронмент Win32**](win32-rdmsenvironment.md)
</dt> </dl>

 

 





