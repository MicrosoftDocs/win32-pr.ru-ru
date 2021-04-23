---
title: ауксусертипе
description: Указывает краткое отображаемое имя приложения и имена приложений.
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- COM раздела реестра Ауксусертипе
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103772569"
---
# <a name="auxusertype"></a><span data-ttu-id="d50b9-104">ауксусертипе</span><span class="sxs-lookup"><span data-stu-id="d50b9-104">AuxUserType</span></span>

<span data-ttu-id="d50b9-105">Указывает краткое отображаемое имя приложения и имена приложений.</span><span class="sxs-lookup"><span data-stu-id="d50b9-105">Specifies an application's short display name and application names.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="d50b9-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="d50b9-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a><span data-ttu-id="d50b9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d50b9-107">Remarks</span></span>

<span data-ttu-id="d50b9-108">Рекомендуемая максимальная длина для *ShortDisplayName* — 15 символов.</span><span class="sxs-lookup"><span data-stu-id="d50b9-108">The recommended maximum length for *ShortDisplayName* is 15 characters.</span></span> <span data-ttu-id="d50b9-109">Это имя используется в меню, включая всплывающие меню.</span><span class="sxs-lookup"><span data-stu-id="d50b9-109">This name is used in menus, including pop-up menus.</span></span>

<span data-ttu-id="d50b9-110">*ApplicationName* должно содержать фактическое имя приложения (например, "Acme Draw 2,0").</span><span class="sxs-lookup"><span data-stu-id="d50b9-110">*ApplicationName* should contain the actual name of the application (such as "Acme Draw 2.0").</span></span> <span data-ttu-id="d50b9-111">Это имя используется в поле **результаты** диалогового окна Специальная **Вставка** .</span><span class="sxs-lookup"><span data-stu-id="d50b9-111">This name is used in the **Results** field of the **Paste Special** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d50b9-112">См. также</span><span class="sxs-lookup"><span data-stu-id="d50b9-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d50b9-113">**Иолеобжект:: Жетусертипе**</span><span class="sxs-lookup"><span data-stu-id="d50b9-113">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




