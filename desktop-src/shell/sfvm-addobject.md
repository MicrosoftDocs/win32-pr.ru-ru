---
description: Добавляет объект в представление оболочки. Используется \_ сообщением шшеллфолдервиев.
title: Сообщение SFVM_ADDOBJECT (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 90394af6-3809-457c-b2f2-5f35187ed45b
api_name:
- SFVM_ADDOBJECT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 0e5b3f0a5b1aed634ab8929b0501d2e23ba40352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997811"
---
# <a name="sfvm_addobject-message"></a><span data-ttu-id="1a374-104">\_Сообщение сфвм ADDOBJECT</span><span class="sxs-lookup"><span data-stu-id="1a374-104">SFVM\_ADDOBJECT message</span></span>

<span data-ttu-id="1a374-105">Добавляет объект в представление оболочки.</span><span class="sxs-lookup"><span data-stu-id="1a374-105">Adds an object to the Shell view.</span></span> <span data-ttu-id="1a374-106">Используется [**\_ сообщением шшеллфолдервиев**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span><span class="sxs-lookup"><span data-stu-id="1a374-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_ADDOBJECT 

    lParam = (LPARAM) pidl;

            
```



## <a name="parameters"></a><span data-ttu-id="1a374-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="1a374-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a374-108">*Пидл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1a374-108">*pidl* \[in\]</span></span>
</dt> <dd><span data-ttu-id="1a374-109">Указатель на объект, который нужно добавить.</span><span class="sxs-lookup"><span data-stu-id="1a374-109">A pointer to the object of interest to add.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a374-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1a374-110">Return value</span></span>

<span data-ttu-id="1a374-111">Возвращает новый идентификатор элемента ListView добавленного объекта, если процесс выполнен успешно; в противном случае возвращает значение-1.</span><span class="sxs-lookup"><span data-stu-id="1a374-111">Returns the new listview item ID of the added object if the process was successful; otherwise, returns -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a374-112">Требования</span><span class="sxs-lookup"><span data-stu-id="1a374-112">Requirements</span></span>



| <span data-ttu-id="1a374-113">Требование</span><span class="sxs-lookup"><span data-stu-id="1a374-113">Requirement</span></span> | <span data-ttu-id="1a374-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1a374-114">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1a374-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a374-115">Minimum supported client</span></span><br/> | <span data-ttu-id="1a374-116">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a374-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1a374-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a374-117">Minimum supported server</span></span><br/> | <span data-ttu-id="1a374-118">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="1a374-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1a374-119">Заголовок</span><span class="sxs-lookup"><span data-stu-id="1a374-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a374-120"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a374-120"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




