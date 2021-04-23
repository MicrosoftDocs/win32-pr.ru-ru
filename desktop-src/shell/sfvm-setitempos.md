---
description: Задает позицию элемента в представлении оболочки. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_SETITEMPOS (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: b89f2d62-095b-4cad-a47e-2d41e122cb3e
api_name:
- SFVM_SETITEMPOS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 450aeabee6e5edeba466e4a5fe64725c13eea32b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272646"
---
# <a name="sfvm_setitempos-message"></a><span data-ttu-id="f1665-104">\_Сообщение сфвм сетитемпос</span><span class="sxs-lookup"><span data-stu-id="f1665-104">SFVM\_SETITEMPOS message</span></span>

<span data-ttu-id="f1665-105">Задает позицию элемента в представлении оболочки.</span><span class="sxs-lookup"><span data-stu-id="f1665-105">Sets the position of an item in the Shell view.</span></span> <span data-ttu-id="f1665-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="f1665-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++

                SFVM_SETITEMPOS 

    lParam = (LPSFV_SETITEMPOS)&sip;

            
```



## <a name="parameters"></a><span data-ttu-id="f1665-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f1665-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1665-108">*модуль SIP* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f1665-108">*sip* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1665-109">Указатель на структуру [**\_ сетитемпос СФВ**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) .</span><span class="sxs-lookup"><span data-stu-id="f1665-109">A pointer to an [**SFV\_SETITEMPOS**](/windows/desktop/api/Shlobj/ns-shlobj-sfv_setitempos) structure.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f1665-110">Требования</span><span class="sxs-lookup"><span data-stu-id="f1665-110">Requirements</span></span>



| <span data-ttu-id="f1665-111">Требование</span><span class="sxs-lookup"><span data-stu-id="f1665-111">Requirement</span></span> | <span data-ttu-id="f1665-112">Значение</span><span class="sxs-lookup"><span data-stu-id="f1665-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f1665-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f1665-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f1665-114">Только для настольных приложений Windows XP с пакетом обновления 1 \[\]</span><span class="sxs-lookup"><span data-stu-id="f1665-114">Windows XP with SP1 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f1665-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f1665-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f1665-116">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f1665-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f1665-117">Header</span><span class="sxs-lookup"><span data-stu-id="f1665-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1665-118"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1665-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




