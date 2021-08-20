---
description: Содержит таблицу основных сведений для всех интерфейсов беспроводной локальной сети, управляемых службой настройки беспроводной связи.
ms.assetid: 5d5fe222-6ca1-4778-9f64-1c6a63467a6c
title: Структура INTFS_KEY_TABLE (Взксапи. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- INTFS_KEY_TABLE
api_type:
- HeaderDef
api_location:
- Wzcsapi.h
ms.openlocfilehash: 5e1aee9708721036fba487edafa901ec701156d44d3f6cb76265d49701925cef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117984984"
---
# <a name="intfs_key_table-structure"></a>\_ \_ Структура таблицы ключей интфс

\[**Интфс \_ \_таблица ключей** больше не поддерживается в Windows Vista и Windows Server 2008. Вместо этого используйте [собственный интерфейс API Wi-Fi](native-wifi-reference.md), который предоставляет аналогичные функциональные возможности. Дополнительные сведения см. [в статье о встроенном API Wi-Fi](about-the-native-wifi-api.md).\]

Структура **\_ \_ таблицы ключей интфс** содержит таблицу основных сведений для всех интерфейсов беспроводной локальной сети, управляемых службой настройки беспроводной связи.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD           dwNumIntfs;
  PINTF_KEY_ENTRY pIntfs;
} INTFS_KEY_TABLE, *PINTFS_KEY_TABLE;
```



## <a name="members"></a>Члены

<dl> <dt>

**двнуминтфс**
</dt> <dd>

Общее число интерфейсов.

</dd> <dt>

**пинтфс**
</dt> <dd>

Указатель на структуру [**\_ \_ записи ключа intf**](intf-key-entry.md) .

</dd> </dl>

## <a name="remarks"></a>Remarks

> [!Note]  
> файл заголовка *взксапи. h* недоступен в Windows SDK.

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP с пакетом обновления 2 (SP2) \[ только классические приложения\]<br/>                                 |
| Минимальная версия сервера<br/> | Windows Только для \[ настольных приложений сервера 2003\]<br/>                                 |
| Окончание поддержки клиента<br/>    | Windows XP с пакетом обновления SP3<br/>                                                       |
| Поддержка конца сервера<br/>    | Windows Server 2003<br/>                                                       |
| Заголовок<br/>                   | <dl> <dt>Взксапи. h</dt> </dl> |



 

 




