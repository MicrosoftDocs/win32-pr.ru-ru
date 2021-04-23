---
title: донотаддаллаппликатионпаккажесторестриктионс
description: Определяет, будут ли вызовы RPC автоматически добавлять \_ \_ идентификаторы безопасности пакетов всех приложений в ограничения com по умолчанию.
ms.assetid: 4DC1237E-F3EF-40EA-8E64-57320F0C4CC5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 800077c61e01cf0b3f76d5a92f8282c7ecca12e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410676"
---
# <a name="donotaddallapplicationpackagestorestrictions"></a><span data-ttu-id="f67d9-103">донотаддаллаппликатионпаккажесторестриктионс</span><span class="sxs-lookup"><span data-stu-id="f67d9-103">DoNotAddAllApplicationPackagesToRestrictions</span></span>

<span data-ttu-id="f67d9-104">Определяет, будут ли вызовы RPC автоматически добавлять \_ \_ идентификаторы безопасности пакетов всех приложений в ограничения com по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f67d9-104">Determines whether RPCSS automatically appends an ALL\_APPLICATION\_PACKAGES SID to COM restrictions by default.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="f67d9-105">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="f67d9-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DoNotAddAllApplicationPackagesToRestrictions = value
```

## <a name="remarks"></a><span data-ttu-id="f67d9-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f67d9-106">Remarks</span></span>

<span data-ttu-id="f67d9-107">Это значение **reg \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="f67d9-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="f67d9-108">Значение</span><span class="sxs-lookup"><span data-stu-id="f67d9-108">Value</span></span> | <span data-ttu-id="f67d9-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f67d9-109">Description</span></span>                                                                               |
|-------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f67d9-110">0</span><span class="sxs-lookup"><span data-stu-id="f67d9-110">0</span></span>     | <span data-ttu-id="f67d9-111">Отключает приложения Магазина Windows при миграции с Windows 7 на Windows 8.</span><span class="sxs-lookup"><span data-stu-id="f67d9-111">Disables Windows Store apps upon migration from Windows 7 to Windows 8.</span></span>                   |
| <span data-ttu-id="f67d9-112">1</span><span class="sxs-lookup"><span data-stu-id="f67d9-112">1</span></span>     | <span data-ttu-id="f67d9-113">Не добавляет \_ идентификатор безопасности "все \_ пакеты приложений" в ограничения com.</span><span class="sxs-lookup"><span data-stu-id="f67d9-113">Does not add the ALL\_APPLICATION\_PACKAGES SID to COM restrictions.</span></span> <span data-ttu-id="f67d9-114">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f67d9-114">This is the default.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f67d9-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f67d9-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f67d9-116">Настройка безопасности для приложений COM</span><span class="sxs-lookup"><span data-stu-id="f67d9-116">Setting Security for COM Applications</span></span>](setting-security-for-com-applications.md)
</dt> </dl>

 

 




