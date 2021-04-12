---
title: IMsRdpClientNonScriptable3 Енаблекредсспсуппорт, свойство
description: Указывает или получает значение, указывающее, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Енаблекредсспсуппорт
- Службы удаленных рабочих столов свойства Енаблекредсспсуппорт, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Енаблекредсспсуппорт
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135767"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a>Свойство IMsRdpClientNonScriptable3:: Енаблекредсспсуппорт

Указывает или получает значение, указывающее, включен ли поставщик службы безопасности учетных данных (CredSSP) для этого подключения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a>Значение свойства

Указывает, включен ли CredSSP для этого соединения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                      |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                                |
| Библиотека типов<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 определен как b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





