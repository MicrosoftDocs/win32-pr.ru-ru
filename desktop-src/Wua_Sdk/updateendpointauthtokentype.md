---
description: Определяет тип токенов, которые могут использоваться для проверки подлинности с помощью конечной точки.
ms.assetid: 2048BD09-056F-47C1-AD2F-998DE6C52EA6
title: Перечисление Упдатиндпоинтаустокентипе (Упдатиндпоинтаус. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UpdateEndpointAuthTokenType
api_type:
- HeaderDef
api_location:
- UpdateEndpointAuth.h
ms.openlocfilehash: b9e3efbff48097dcede12d5c8d3117171ef622f20a3bf017b12c6d3ce13a1c00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118814716"
---
# <a name="updateendpointauthtokentype-enumeration"></a>Перечисление Упдатиндпоинтаустокентипе

Определяет тип токенов, которые могут использоваться для проверки подлинности с помощью конечной точки.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagUpdateEndpointAuthTokenType { 
  ueattInvalidTokenType  = 0x0,
  ueattSAML11Token       = 0X1
} UpdateEndpointAuthTokenType;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="ueattInvalidTokenType"></span><span id="ueattinvalidtokentype"></span><span id="UEATTINVALIDTOKENTYPE"></span>**уеаттинвалидтокентипе**
</dt> <dd>

Токен проверки подлинности не требуется.

</dd> <dt>

<span id="ueattSAML11Token"></span><span id="ueattsaml11token"></span><span id="UEATTSAML11TOKEN"></span>**ueattSAML11Token**
</dt> <dd>

Токен проверки подлинности для конечной точки является маркером WS-Security SAML (язык разметки зявлений системы безопасности (SAML)) 1,1.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                        |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                              |
| Заголовок<br/>                   | <dl> <dt>Упдатиндпоинтаус. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Упдатиндпоинтаус. idl</dt> </dl> |



 

 




