---
description: Для получения идентификаторов GUID поставщика или класса трассировки событий можно использовать средство Uuidgen.exe или Guidgen.exe.
ms.assetid: 07483a78-ee67-4586-a75b-d376aa3351b7
title: Получение идентификатора GUID поставщика и класса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c12554cdb39459d824bf6622cd9d50e52f8c788d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985716"
---
# <a name="obtaining-a-provider-and-class-guid"></a><span data-ttu-id="5a0ce-103">Получение идентификатора GUID поставщика и класса</span><span class="sxs-lookup"><span data-stu-id="5a0ce-103">Obtaining a Provider and Class GUID</span></span>

<span data-ttu-id="5a0ce-104">Для получения идентификаторов GUID поставщика или класса трассировки событий можно использовать средство Uuidgen.exe или Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="5a0ce-104">To obtain a provider GUID or event trace class GUIDs, you can use the Uuidgen.exe or Guidgen.exe tool.</span></span>

<span data-ttu-id="5a0ce-105">При использовании средства Uuidgen.exe используйте параметр-d, чтобы создать \_ макрос define GUID C, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="5a0ce-105">If you use the Uuidgen.exe tool, use the -d option to create a DEFINE\_GUID C macro, as shown in the following example.</span></span> <span data-ttu-id="5a0ce-106">Для получения сведений об использовании средства Uuidgen.exe используйте параметр-?</span><span class="sxs-lookup"><span data-stu-id="5a0ce-106">For information about using the Uuidgen.exe tool, use the -?</span></span> <span data-ttu-id="5a0ce-107">(Создайте ветвь для и запустите запрос на вытягивание).</span><span class="sxs-lookup"><span data-stu-id="5a0ce-107">option.</span></span> <span data-ttu-id="5a0ce-108">Если вы используете макрос DEFINE \_ GUID C для определения идентификатора GUID, необходимо включить \# Определение инитгуид перед определениями GUID, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="5a0ce-108">If you use the DEFINE\_GUID C macro to define your GUID, you must include \#define INITGUID before your GUID definitions, as shown in the following example.</span></span>

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

<span data-ttu-id="5a0ce-109">Пакет средств разработки программного обеспечения Microsoft Windows (SDK) и Microsoft Visual Studio включают в себя средство Guidgen.exe.</span><span class="sxs-lookup"><span data-stu-id="5a0ce-109">The Microsoft Windows Software Development Kit (SDK) and Microsoft Visual Studio include the Guidgen.exe tool.</span></span> <span data-ttu-id="5a0ce-110">Средство Guidgen.exe имеет пользовательский интерфейс, позволяющий выбрать один из нескольких форматов.</span><span class="sxs-lookup"><span data-stu-id="5a0ce-110">The Guidgen.exe tool has a user interface that lets you select from several formats.</span></span> <span data-ttu-id="5a0ce-111">Следует использовать формат, который создает статический GUID константы, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="5a0ce-111">You should use the format that creates a static constant GUID, as shown in the following example.</span></span>

``` syntax
// {7C214FB1-9CAC-4b8d-BAED-7BF48BF63BB3}
static const GUID ProviderGuid = 
{ 0x7c214fb1, 0x9cac, 0x4b8d, { 0xba, 0xed, 0x7b, 0xf4, 0x8b, 0xf6, 0x3b, 0xb3 } };
```

 

 



