---
title: IMsRdpClientNonScriptable3 Коннектионбартекст, свойство
description: Задает или получает текст для обновления панели подключения.
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Коннектионбартекст
- Службы удаленных рабочих столов свойства Коннектионбартекст, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Коннектионбартекст
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89dac8f704f5ecaa7bd521af10f05fd1c56d2adebff70827862478847a782faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941597"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a>Свойство IMsRdpClientNonScriptable3:: Коннектионбартекст

Задает или получает текст для обновления панели подключения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a>Значение свойства

Задает текстовую строку, отображаемую на панели подключения.

## <a name="remarks"></a>Remarks

Необходимо вызвать метод **IMsRdpClientNonScriptable3::p UT \_ коннектионбартекст** перед вызовом метода [**имстсксекуредсеттингс::p UT \_**](imstscsecuredsettings-fullscreen.md) , а также метода [**имсрдпклиент::p UT \_**](imsrdpclient-fullscreen.md) .

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

 

 





