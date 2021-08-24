---
description: Для получения идентификаторов GUID поставщика или класса трассировки событий можно использовать средство Uuidgen.exe или Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Получение идентификатора GUID поставщика и класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c480a45a5a826d3f258ab267e39db87bc85fad799fef5d7397a7c900f4872f22
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914354"
---
# <a name="obtaining-a-provider-and-class-guid"></a>Получение идентификатора GUID поставщика и класса

Для получения идентификаторов GUID поставщика или класса трассировки событий можно использовать средство Uuidgen.exe или Guidgen.exe.

При использовании средства Uuidgen.exe используйте параметр-d, чтобы создать \_ макрос define GUID C, как показано в следующем примере. Для получения сведений об использовании средства Uuidgen.exe используйте параметр-? (Создайте ветвь для и запустите запрос на вытягивание). Если вы используете макрос DEFINE \_ GUID C для определения идентификатора GUID, необходимо включить \# Определение инитгуид перед определениями GUID, как показано в следующем примере.

``` syntax
#define INITGUID

DEFINE_GUID (
  ProviderGuid,
  0xf4dc272d, 
  0x88dd, 
  0x4472, 
  0xa3, 0xb1, 0xcb, 0x6d, 0xa4, 0x86, 0xf0, 0xbe
  );
```

пакет средств разработки Microsoft Windows Software Development Kit (SDK) и Microsoft Visual Studio содержит средство Guidgen.exe. Средство Guidgen.exe имеет пользовательский интерфейс, позволяющий выбрать один из нескольких форматов. Следует использовать формат, который создает статический GUID константы, как показано в следующем примере.

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



