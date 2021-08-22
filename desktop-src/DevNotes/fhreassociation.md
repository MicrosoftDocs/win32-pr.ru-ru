---
description: Представляет функцию повторной связи с журналом файлов, которая позволяет пользователю восстановить связь с целевым объектом резервного копирования, который использовался тем же пользователем в прошлом. Повторное связывание выполняется путем вызова методов интерфейса ИфхреассоЦиатион.
ms.assetid: BB81F8ED-4DFB-4FA5-B3ED-ACBAB32BBE3D
title: Класс ФхреассоЦиатион (Фхкфг. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FhReassociation
api_type:
- COM
api_location:
- Fhcfg.idl
ms.openlocfilehash: f4b8cb55ce4b374f7f17f16044811a930623fc777a028ee98b5d8726bf714cce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538514"
---
# <a name="fhreassociation-class"></a>Класс ФхреассоЦиатион

Представляет функцию повторной связи с журналом файлов, которая позволяет пользователю восстановить связь с целевым объектом резервного копирования, который использовался тем же пользователем в прошлом. Повторное связывание выполняется путем вызова методов интерфейса [**ифхреассоЦиатион**](/windows/desktop/api/Fhcfg/nn-fhcfg-ifhreassociation) .

## <a name="when-to-implement"></a>Когда следует реализовывать

API истории файлов реализует этот класс. Чтобы создать экземпляр этого класса, используйте функцию [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) .

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                           |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                 |
| Заголовок<br/>                   | <dl> <dt>Фхкфг. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Фхкфг. idl</dt> </dl> |



 

 
