---
title: Метод Провисионинженумератежобс класса Win32_RDMSVirtualDesktopCollection
description: Перечисляет задания подготовки виртуальных рабочих столов для этой службы.
ms.assetid: 4bd2b03f-ba8c-483e-af09-270424f9b1ed
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионинженумератежобс
- Службы удаленных рабочих столов метода Провисионинженумератежобс, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Провисионинженумератежобс
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningEnumerateJobs
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b24ef80acdb29c75327447f61db7dae1689a883f69c9e19ef199710de216fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118350226"
---
# <a name="provisioningenumeratejobs-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод Провисионинженумератежобс \_ класса Win32 рдмсвиртуалдесктопколлектион

Перечисляет задания подготовки виртуальных рабочих столов для этой службы.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ProvisioningEnumerateJobs(
  [in]  uint32 JobType,
  [in]  string CollectionAlias,
  [out] string JobGuids[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*JobType* \[ окне\]
</dt> <dd>

Целое число, указывающее тип задания для перечисления.

Этому параметру можно присвоить одно из следующих значений:

<dt>

0
</dt> <dd>

Выполняемые задания

</dd> <dt>

1
</dt> <dd>

Завершенные задания

</dd> </dl> </dd> <dt>

*Коллектионалиас* \[ окне\]
</dt> <dd>

Псевдоним коллекции виртуальных рабочих столов для перечисления. Значение по умолчанию для этого параметра равно FALSE, что указывает на то, что все выполняемые задания должны быть перечислены.

</dd> <dt>

*Жобгуидс* \[ заполняет\]
</dt> <dd>

Массив, содержащий **идентификаторы GUID** заданий подготовки для перечисления.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 при успешном выполнении, в противном случае возвращает код ошибки WMI.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Ни одна версия не поддерживается<br/>                                                                   |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                              |
| Пространство имен<br/>                | Корневой \\ \\ rdms CIMv2<br/>                                                                |
| MOF<br/>                      | <dl> <dt>Рдманажемент. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Рдмсвиртуалдесктопколлектион Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





