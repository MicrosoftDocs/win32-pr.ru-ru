---
title: Метод Провисионингжобжетрепорт класса Win32_RDMSVirtualDesktopCollection
description: Возвращает отчет о состоянии задания подготовки виртуальных рабочих столов.
ms.assetid: 8fc03fed-0838-4530-9b0f-0f561d76769d
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов метода Провисионингжобжетрепорт
- Службы удаленных рабочих столов метода Провисионингжобжетрепорт, класс Win32_RDMSVirtualDesktopCollection
- Класс Win32_RDMSVirtualDesktopCollection службы удаленных рабочих столов, метод Провисионингжобжетрепорт
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobGetReport
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6605402c6ed6c0269b9971922bdefd48f265c4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672715"
---
# <a name="provisioningjobgetreport-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Метод Провисионингжобжетрепорт \_ класса Win32 рдмсвиртуалдесктопколлектион

Возвращает отчет о состоянии задания подготовки виртуальных рабочих столов.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ProvisioningJobGetReport(
  [in]  string JobGuid,
  [out] string JobReportXml
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Жобгуид* \[ окне\]
</dt> <dd>

**Идентификатор GUID** , однозначно определяющий задание подготовки.

</dd> <dt>

*Жобрепортксмл* \[ заполняет\]
</dt> <dd>

Строка, содержащая отчет в формате XML.

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

[**\_Рдмсвиртуалдесктопколлектион Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





