---
description: Перечисление наборов символов BLOB-объектов указывает кодировку, \_ \_ используемую текущим объектом-blobом для конференций.
ms.assetid: 79131b84-19b5-492b-a44e-9d47c365b298
title: Перечисление BLOB_CHARACTER_SET (Сдпблб. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66b180a8574f1643a5fc1be134be99c951faaf1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675717"
---
# <a name="blob_character_set-enumeration"></a>\_Перечисление наборов символов BLOB-объектов \_

\[ В Windows Vista, Windows Server 2008 и последующих версиях операционной системы нельзя использовать встречные средства и элементы управления Конференц-телефонией и интерфейсы. API клиента RTC предоставляет аналогичные функциональные возможности.\]

Перечисление **\_ \_ наборов символов BLOB-объектов** указывает кодировку, используемую текущим объектом-blobом для конференций.

## <a name="syntax"></a>Синтаксис


```C++
} BLOB_CHARACTER_SET;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="BCS_ASCII"></span><span id="bcs_ascii"></span>**код \_ ASCII для BCS**
</dt> <dd>

Стандартный формат ASCII.

</dd> <dt>

<span id="BCS_UTF7"></span><span id="bcs_utf7"></span>**\_UTF7 BCS**
</dt> <dd>

Семь-разрядный формат преобразования Юникода. Для получения дополнительных сведений об этом формате выполните поиск в Интернете по RFC 1642.

</dd> <dt>

<span id="BCS_UTF8"></span><span id="bcs_utf8"></span>**Синхронизация BCS (в \_ UTF8)**
</dt> <dd>

Формат преобразования UCS 8. Чтобы получить подробные сведения об этом формате, выполните поиск в Интернете для ISO (Международная организация по стандартизации) и IEC (IEC) документа ISO/IEC JTC1/SC2/WG2 N 1036, датированный 1, 1994, в редакторе проектов WG2.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-------------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 3,0 или более поздней версии<br/>                                               |
| Header<br/>       | <dl> <dt>Сдпблб. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**итдиректорйобжектконференце**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference)
</dt> <dt>

[**получить \_ кодировку**](itconferenceblob-get-characterset.md)
</dt> <dt>

[**Ini**](itconferenceblob-init.md)
</dt> <dt>

[**сетконференцеблоб**](itconferenceblob-setconferenceblob.md)
</dt> </dl>

 

 




