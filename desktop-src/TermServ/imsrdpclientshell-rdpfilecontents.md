---
title: Имсрдпклиентшелл Рдпфилеконтентс, свойство
description: Указывает или получает содержимое файла протокол удаленного рабочего стола (RDP) для запуска из удаленный рабочий стол Веб-доступ (RD Веб-доступ) или с другого веб-портала.
ms.assetid: fcf37221-0fd5-41fd-83da-7fafc1aff944
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Рдпфилеконтентс
- Службы удаленных рабочих столов свойства Рдпфилеконтентс, интерфейс Имсрдпклиентшелл
- Службы удаленных рабочих столов интерфейса Имсрдпклиентшелл, свойство Рдпфилеконтентс
topic_type:
- apiref
api_name:
- IMsRdpClientShell.RdpFileContents
- IMsRdpClientShell.get_RdpFileContents
- IMsRdpClientShell.put_RdpFileContents
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2d1c682c06415757f29f2226f48970f4268800
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681974"
---
# <a name="imsrdpclientshellrdpfilecontents-property"></a>Свойство Имсрдпклиентшелл:: Рдпфилеконтентс

Указывает или получает содержимое файла протокол удаленного рабочего стола (RDP) для запуска из удаленный рабочий стол Веб-доступ (RD Веб-доступ) или с другого веб-портала.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_RdpFileContents(
  [in]  BSTR newVal
);

HRESULT get_RdpFileContents(
  [out] BSTR *pszRdpFile
);
```



## <a name="property-value"></a>Значение свойства

Указывает содержимое RDP-файла, которое должно быть запущено с портала.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                               |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                         |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ имсрдпклиентшелл определен как d012ae6d-c19a-4bfe-b367-201f8911f134<br/>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**имсрдпклиентшелл**](imsrdpclientshell.md)
</dt> </dl>

 

 





