---
description: 'Позволяет объекту обратного вызова предоставить страницу для добавления в страницу свойств выбранного объекта. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_ADDPROPERTYPAGES (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 54f67d0e-6089-4e75-a547-5313794e1512
api_name:
- SFVM_ADDPROPERTYPAGES
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e5f3e1f39b457bce105a8ac2b4be8b5939435615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997810"
---
# <a name="sfvm_addpropertypages-message"></a><span data-ttu-id="b9365-104">\_Сообщение сфвм аддпропертипажес</span><span class="sxs-lookup"><span data-stu-id="b9365-104">SFVM\_ADDPROPERTYPAGES message</span></span>

<span data-ttu-id="b9365-105">Позволяет объекту обратного вызова предоставить страницу для **добавления в страницу свойств выбранного** объекта.</span><span class="sxs-lookup"><span data-stu-id="b9365-105">Allows the callback object to provide a page to add to the **Properties** property sheet of the selected object.</span></span> <span data-ttu-id="b9365-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="b9365-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_ADDPROPERTYPAGES 

    lParam = (LPARAM)(SFVM_PROPPAGE_DATA*) pData;

            
```



## <a name="parameters"></a><span data-ttu-id="b9365-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="b9365-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b9365-108">*pData* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="b9365-108">*pData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b9365-109">Адрес структуры [**\_ \_ данных сфвм**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) .</span><span class="sxs-lookup"><span data-stu-id="b9365-109">The address of a [**SFVM\_PROPPAGE\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_proppage_data) structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9365-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="b9365-110">Remarks</span></span>

<span data-ttu-id="b9365-111">Это сообщение играет по сути ту же функцию, что и [**ишеллпропшитекст:: аддпажес**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span><span class="sxs-lookup"><span data-stu-id="b9365-111">This message serves essentially the same function as [**IShellPropSheetExt::AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages).</span></span> <span data-ttu-id="b9365-112">Дополнительные сведения см. в статье [Создание обработчиков страницы свойств](propsheet-handlers.md) .</span><span class="sxs-lookup"><span data-stu-id="b9365-112">See [Creating Property Sheet Handlers](propsheet-handlers.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9365-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b9365-113">Requirements</span></span>



| <span data-ttu-id="b9365-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b9365-114">Requirement</span></span> | <span data-ttu-id="b9365-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b9365-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b9365-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b9365-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b9365-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9365-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b9365-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b9365-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b9365-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b9365-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b9365-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b9365-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9365-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9365-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
