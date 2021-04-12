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
ms.openlocfilehash: 91f25708e79be4f85c4200bd690404ff39f567d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343895"
---
# <a name="intf_key_entry-structure"></a>\_ \_ Структура ввода ключа intf

\[**Intf \_ \_Запись ключа** больше не поддерживается в Windows Vista и windows Server 2008. Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности. Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]

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

## <a name="remarks"></a>Комментарии

> [!Note]  
> Файл заголовка *взксапи. h* недоступен в Windows SDK.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для настольных приложений Windows XP с пакетом обновления 2 \[\]<br/>                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2003\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления 3 (SP3)<br/>                                                       |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Header<br/>                   | <dl> <dt>Взксапи. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Таблица ключей \_ интфс**](intfs-key-table.md)
</dt> <dt>

[**взценуминтерфацес**](wzcenuminterfaces.md)
</dt> </dl>

 

 




