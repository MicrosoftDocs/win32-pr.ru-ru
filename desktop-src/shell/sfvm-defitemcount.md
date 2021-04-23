---
description: 'Позволяет объекту обратного вызова указывать количество элементов в представлении папки. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_DEFITEMCOUNT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 62306eaa-e52e-432b-9233-d990519d5739
api_name:
- SFVM_DEFITEMCOUNT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 4e3f746e422428ab9f925cf4ff3f460ccd578367
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998755"
---
# <a name="sfvm_defitemcount-message"></a><span data-ttu-id="d1a3f-104">\_Сообщение сфвм дефитемкаунт</span><span class="sxs-lookup"><span data-stu-id="d1a3f-104">SFVM\_DEFITEMCOUNT message</span></span>

<span data-ttu-id="d1a3f-105">Позволяет объекту обратного вызова указывать количество элементов в представлении папки.</span><span class="sxs-lookup"><span data-stu-id="d1a3f-105">Allows the callback object to specify the number of items in the folder view.</span></span> <span data-ttu-id="d1a3f-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="d1a3f-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_DEFITEMCOUNT 

    lParam = (LPARAM)(UINT*) cItems;

            
```



## <a name="parameters"></a><span data-ttu-id="d1a3f-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d1a3f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1a3f-108">*Цитемс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d1a3f-108">*cItems* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d1a3f-109">Число элементов в представлении папки.</span><span class="sxs-lookup"><span data-stu-id="d1a3f-109">The number of items in the folder view.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1a3f-110">Требования</span><span class="sxs-lookup"><span data-stu-id="d1a3f-110">Requirements</span></span>



| <span data-ttu-id="d1a3f-111">Требование</span><span class="sxs-lookup"><span data-stu-id="d1a3f-111">Requirement</span></span> | <span data-ttu-id="d1a3f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="d1a3f-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a3f-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d1a3f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d1a3f-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d1a3f-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d1a3f-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d1a3f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d1a3f-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d1a3f-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d1a3f-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d1a3f-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1a3f-118"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="d1a3f-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
