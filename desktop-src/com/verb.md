---
title: Команда
description: Указывает команды для регистрации в приложении.
ms.assetid: bfcad36d-a52a-4117-bf0b-6135b197a7ee
keywords:
- Раздел реестра verb-COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ef025ee0807ca3e75577f26f81951db22dfb0ac
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105710371"
---
# <a name="verb"></a><span data-ttu-id="fac8e-104">Команда</span><span class="sxs-lookup"><span data-stu-id="fac8e-104">Verb</span></span>

<span data-ttu-id="fac8e-105">Указывает команды для регистрации в приложении.</span><span class="sxs-lookup"><span data-stu-id="fac8e-105">Specifies the verbs to be registered for an application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="fac8e-106">Запись реестра</span><span class="sxs-lookup"><span data-stu-id="fac8e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Verb
         1 = verb1
         2 = verb2
         3 = ...
```

## <a name="remarks"></a><span data-ttu-id="fac8e-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fac8e-107">Remarks</span></span>

<span data-ttu-id="fac8e-108">Каждая команда является значением **reg \_ SZ** в форме "*имя*, *\_ флаг меню*, *\_ флаг команды*".</span><span class="sxs-lookup"><span data-stu-id="fac8e-108">Each verb is a **REG\_SZ** value of the form "*name*, *menu\_flag*, *verb\_flag*".</span></span> <span data-ttu-id="fac8e-109">Глаголы должны быть пронумерованы последовательно.</span><span class="sxs-lookup"><span data-stu-id="fac8e-109">Verbs must be numbered consecutively.</span></span>

<span data-ttu-id="fac8e-110">*Имя* описывает, как команда добавляется вызовом функции [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua) .</span><span class="sxs-lookup"><span data-stu-id="fac8e-110">The *name* describes how the verb is appended by an [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) function call.</span></span> <span data-ttu-id="fac8e-111">Например, "&Play".</span><span class="sxs-lookup"><span data-stu-id="fac8e-111">For example, "&Play".</span></span>

<span data-ttu-id="fac8e-112">Значение *\_ флага меню* указывает, как команда должна отображаться в меню.</span><span class="sxs-lookup"><span data-stu-id="fac8e-112">The *menu\_flag* value indicates how the verb should appear in the menu.</span></span> <span data-ttu-id="fac8e-113">Поддерживаются все флаги, поддерживаемые [**аппендмену**](/windows/win32/api/winuser/nf-winuser-appendmenua) , за исключением \_ всплывающего изображения MF, MF \_ овнердрав и MF \_ .</span><span class="sxs-lookup"><span data-stu-id="fac8e-113">All flags supported by [**AppendMenu**](/windows/win32/api/winuser/nf-winuser-appendmenua) are supported, except for MF\_BITMAP, MF\_OWNERDRAW, and MF\_POPUP.</span></span>

<span data-ttu-id="fac8e-114">Значение *\_ флага команды* описывает атрибуты команд.</span><span class="sxs-lookup"><span data-stu-id="fac8e-114">The *verb\_flag* value describes attributes of the verbs.</span></span> <span data-ttu-id="fac8e-115">Используйте одно из значений из [**олевербаттриб**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)или 0.</span><span class="sxs-lookup"><span data-stu-id="fac8e-115">Use one of the values from [**OLEVERBATTRIB**](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib), or 0.</span></span>

<span data-ttu-id="fac8e-116">Дополнительные сведения см. в статьях [**олеверб**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**Иолеобжект::D оверб**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb)и [**иолеобжект:: енумвербс**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span><span class="sxs-lookup"><span data-stu-id="fac8e-116">For more information, see [**OLEVERB**](/windows/win32/api/oleidl/ns-oleidl-oleverb), [**IOleObject::DoVerb**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-doverb), and [**IOleObject::EnumVerbs**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-enumverbs).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fac8e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="fac8e-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac8e-118">**аппендмену**</span><span class="sxs-lookup"><span data-stu-id="fac8e-118">**AppendMenu**</span></span>](/windows/win32/api/winuser/nf-winuser-appendmenua)
</dt> <dt>

[<span data-ttu-id="fac8e-119">**олеверб**</span><span class="sxs-lookup"><span data-stu-id="fac8e-119">**OLEVERB**</span></span>](/windows/win32/api/oleidl/ns-oleidl-oleverb)
</dt> <dt>

[<span data-ttu-id="fac8e-120">**олевербаттриб**</span><span class="sxs-lookup"><span data-stu-id="fac8e-120">**OLEVERBATTRIB**</span></span>](/windows/win32/api/oleidl/ne-oleidl-oleverbattrib)
</dt> </dl>

 

 