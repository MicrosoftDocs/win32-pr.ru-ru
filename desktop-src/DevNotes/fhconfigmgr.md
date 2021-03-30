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
ms.openlocfilehash: 083ce344e44035b5872d91ad14465659defc8229
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895845"
---
# <a name="fhconfigmgr-class"></a>Класс Фхконфигмгр

Представляет конфигурацию истории файлов пользователя, под которым создается объект **фхконфигмгр** . Все операции настройки выполняются путем вызова методов интерфейса [**ифхконфигмгр**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhconfigmgr) .

## <a name="when-to-implement"></a>Когда следует реализовывать

API истории файлов реализует этот класс. Чтобы создать экземпляр этого класса, используйте функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                           |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Фхкфг. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Фхкфг. idl</dt> </dl> |



 

 
