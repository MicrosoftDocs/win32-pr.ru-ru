---
description: 'Позволяет объекту обратного вызова указать режим представления. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_DEFVIEWMODE (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5118fc81-490f-4d76-9361-0d6af0c4b4c0
api_name:
- SFVM_DEFVIEWMODE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8d57bb61b2b938947d0290345215e3735d9d8763
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997922"
---
# <a name="sfvm_defviewmode-message"></a><span data-ttu-id="0084b-104">\_Сообщение сфвм дефвиевмоде</span><span class="sxs-lookup"><span data-stu-id="0084b-104">SFVM\_DEFVIEWMODE message</span></span>

<span data-ttu-id="0084b-105">Позволяет объекту обратного вызова указать режим представления.</span><span class="sxs-lookup"><span data-stu-id="0084b-105">Allows the callback object to specify the view mode.</span></span> <span data-ttu-id="0084b-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="0084b-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFVIEWMODE 

    lParam = (LPARAM)(FOLDERVIEWMODE*) pViewMode;

            
```



## <a name="parameters"></a><span data-ttu-id="0084b-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="0084b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0084b-108">*пвиевмоде* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0084b-108">*pViewMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0084b-109">Одно из значений перечисляемого типа [**фолдервиевмоде**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) .</span><span class="sxs-lookup"><span data-stu-id="0084b-109">One of the values from the [**FOLDERVIEWMODE**](/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folderviewmode) enumerated type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0084b-110">Требования</span><span class="sxs-lookup"><span data-stu-id="0084b-110">Requirements</span></span>



| <span data-ttu-id="0084b-111">Требование</span><span class="sxs-lookup"><span data-stu-id="0084b-111">Requirement</span></span> | <span data-ttu-id="0084b-112">Значение</span><span class="sxs-lookup"><span data-stu-id="0084b-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0084b-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0084b-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0084b-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0084b-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0084b-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0084b-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0084b-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0084b-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0084b-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0084b-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0084b-118"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="0084b-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
