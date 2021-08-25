---
title: IMsRdpClientNonScriptable3 Неготиатесекуритилайер, свойство
description: Указывает или получает значение, указывающее, включен ли уровень безопасности согласования для соединения.
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, интерфейс IMsRdpClientNonScriptable3
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable3, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, интерфейс IMsRdpClientNonScriptable4
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable4, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, интерфейс IMsRdpClientNonScriptable5
- Службы удаленных рабочих столов интерфейса IMsRdpClientNonScriptable5, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient5
- Службы удаленных рабочих столов объекта MsRdpClient5, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient6
- Службы удаленных рабочих столов объекта MsRdpClient6, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient7
- Службы удаленных рабочих столов объекта MsRdpClient7, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient8
- Службы удаленных рабочих столов объекта MsRdpClient8, свойство Неготиатесекуритилайер
- Службы удаленных рабочих столов свойства Неготиатесекуритилайер, объект MsRdpClient9
- Службы удаленных рабочих столов объекта MsRdpClient9, свойство Неготиатесекуритилайер
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13f87abb5323289e60e3d29fa93d5e858a9a755224e7161ba28970ef5ccb186f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119771554"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a>Свойство IMsRdpClientNonScriptable3:: Неготиатесекуритилайер

Указывает или получает значение, указывающее, включен ли уровень безопасности согласования для соединения.

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a>Значение свойства

Указывает, следует ли включить согласование уровня безопасности.

## <a name="remarks"></a>Remarks

Если это свойство имеет значение **Variant \_ FALSE** и проверка подлинности на уровне сети (NLA) включено в клиентской операционной системе, клиент не будет согласовывать уровень безопасности и вместо этого будет использовать NLA для защиты RDP-подключения. Если для этого свойства задано **значение \_ true**, клиент будет согласовываться между NLA и базовой безопасностью RDP.

> [!Note]  
> отключение согласования уровня безопасности возможно только при подключении к серверу узла сеансов удаленный рабочий стол (к узлу сеансов удаленных рабочих столов) под управлением Windows Vista или более поздних операционных систем. Если это свойство включено и клиент пытается подключиться к серверу узла сеансов удаленных рабочих столов под управлением более ранней операционной системы, произойдет сбой подключения.

 

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

 

 





