---
title: Структура Мрмресаурцеиндексермессаже (Мрмресаурцеиндексер. h)
description: Представляет сообщение, созданное индексатором ресурсов. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки.
ms.assetid: E00065E6-A468-4ACD-AF89-434E4F5025A4
keywords:
- Меню структуры Мрмресаурцеиндексермессаже и другие ресурсы
- Меню указателя структуры Пмрмресаурцеиндексермессаже и другие ресурсы
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessage
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5073c4f74852d341d7f0711a34abe4459dcbaa79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988332"
---
# <a name="mrmresourceindexermessage-structure"></a>Структура Мрмресаурцеиндексермессаже

\[Некоторые сведения относятся к предварительно выпущенному продукту, который может быть значительно изменен перед коммерческой выпуском. Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.\]

Представляет сообщение, созданное индексатором ресурсов. Дополнительные сведения и пошаговые руководства по использованию этих API см. в разделе [пакетные API индексирования ресурсов (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Синтаксис


```C++
typedef struct _MrmResourceIndexerMessage {
  MrmResourceIndexerMessageSeverity severity;
  ULONG                             id;
  PCWSTR                            text;
} MrmResourceIndexerMessage, *PMrmResourceIndexerMessage;
```



## <a name="members"></a>Члены

<dl> <dt>

**severity**
</dt> <dd>

Тип: **[ **мрмресаурцеиндексермессажесеверити**](mrmresourceindexermessageseverity.md)**

</dd> <dd>

Значение, указывающее серьезность сообщения.

</dd> <dt>

**id**
</dt> <dd>

Тип: **ulong**

</dd> <dd>

Уникальный идентификатор сообщения.

</dd> <dt>

**text**
</dt> <dd>

Тип: **пквстр**

</dd> <dd>

Текст сообщения. Не освобождайте этот указатель; память принадлежит операционной системе.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1803\]<br/>                                       |
| Минимальная версия сервера<br/> | \[Только классические приложения Windows Server\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>Мрмресаурцеиндексер. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы API индексирования ресурсов пакета (PRI) и пользовательские системы сборки](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

