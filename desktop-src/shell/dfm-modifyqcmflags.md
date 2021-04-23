---
description: 'Позволяет обратному вызову изменять \_ значения CFM XXX, переданные в IContextMenu:: куериконтекстмену.'
title: Сообщение DFM_MODIFYQCMFLAGS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896890"
---
# <a name="dfm_modifyqcmflags-message"></a><span data-ttu-id="94569-103">\_Сообщение DFM модификкмфлагс</span><span class="sxs-lookup"><span data-stu-id="94569-103">DFM\_MODIFYQCMFLAGS message</span></span>

<span data-ttu-id="94569-104">Позволяет обратному вызову изменять \_ значения CFM XXX, переданные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="94569-104">Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="94569-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="94569-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94569-106">*пуневфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94569-106">*puNewFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94569-107">Указатель на новые значения флагов.</span><span class="sxs-lookup"><span data-stu-id="94569-107">A pointer to the new flag values.</span></span>

</dd> <dt>

<span data-ttu-id="94569-108">*уфлагс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="94569-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94569-109">Флаги, указывающие, как можно изменить контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="94569-109">Flags that specify how the context menu can be changed.</span></span> <span data-ttu-id="94569-110">Этот параметр использует значения КМФ \_ xxx, описанные в [**IContextMenu:: куериконтекстмену**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span><span class="sxs-lookup"><span data-stu-id="94569-110">This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94569-111">Требования</span><span class="sxs-lookup"><span data-stu-id="94569-111">Requirements</span></span>



| <span data-ttu-id="94569-112">Требование</span><span class="sxs-lookup"><span data-stu-id="94569-112">Requirement</span></span> | <span data-ttu-id="94569-113">Значение</span><span class="sxs-lookup"><span data-stu-id="94569-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="94569-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94569-114">Minimum supported client</span></span><br/> | <span data-ttu-id="94569-115">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="94569-115">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="94569-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94569-116">Minimum supported server</span></span><br/> | <span data-ttu-id="94569-117">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="94569-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="94569-118">Header</span><span class="sxs-lookup"><span data-stu-id="94569-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="94569-119"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="94569-119"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




