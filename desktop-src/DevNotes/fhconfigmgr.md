---
description: Представляет конфигурацию истории файлов пользователя, под которым создается объект Фхконфигмгр. Все операции настройки выполняются путем вызова методов интерфейса Ифхконфигмгр.
ms.assetid: CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788
title: Класс Фхконфигмгр (Фхкфг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhConfigMgr
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: 700e96b72e3b23fa83a384a68bd2723ae244d69b0b10ed47db10843793166f40
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058974"
---
# <a name="fhconfigmgr-class"></a>Класс Фхконфигмгр

Представляет конфигурацию истории файлов пользователя, под которым создается объект **фхконфигмгр** . Все операции настройки выполняются путем вызова методов интерфейса [**ифхконфигмгр**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) .

## <a name="when-to-implement"></a>Когда следует реализовывать

API истории файлов реализует этот класс. Чтобы создать экземпляр этого класса, используйте функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Фхкфг. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Фхкфг. idl</dt> </dl> |



 

 
