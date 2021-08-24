---
description: Хранит основные сведения об интерфейсе беспроводной локальной сети, управляемом службой настройки беспроводной связи.
ms.assetid: 5e689fd0-27d9-48eb-8983-96d7918be1cd
title: Структура INTF_KEY_ENTRY (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTF_KEY_ENTRY
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 8d14c65d49d7ed28e2756c2a690cb4a7efa9000417e896a206710bf4365f8cd4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065154"
---
# <a name="intf_key_entry-structure"></a>\_ \_ Структура ввода ключа intf

\[**Intf \_ \_запись ключа** больше не поддерживается для Windows Vista и Windows Server 2008. Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности. Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]

В **структуре \_ \_ ввода ключа intf** хранятся основные сведения об интерфейсе беспроводной локальной сети, управляемом службой настройки беспроводной связи.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  LPWSTR wszGuid;
} INTF_KEY_ENTRY, *PINTF_KEY_ENTRY;
```



## <a name="members"></a>Члены

<dl> <dt>

**всзгуид**
</dt> <dd>

Указатель на идентификатор GUID интерфейса, представленный в виде строки в Юникоде в следующем формате: "{XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}".

</dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> файл заголовка *взксапи. h* недоступен в Windows SDK.

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления SP3<br/>                                                       |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Взксапи. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Таблица ключей \_ интфс**](intfs-key-table.md)
</dt> <dt>

[**взценуминтерфацес**](wzcenuminterfaces.md)
</dt> </dl>

 

 




