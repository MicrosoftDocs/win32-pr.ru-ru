---
description: 'Позволяет объекту обратного вызова добавлять кнопки на панель инструментов. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETBUTTONINFO (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 983652ed-7309-46aa-a6c9-7516411ba5ac
api_name:
- SFVM_GETBUTTONINFO
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: d0db40f7c1f54cd13d54765ba34a8eab31246809
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985773"
---
# <a name="sfvm_getbuttoninfo-message"></a><span data-ttu-id="d68f6-104">\_Сообщение сфвм жетбуттонинфо</span><span class="sxs-lookup"><span data-stu-id="d68f6-104">SFVM\_GETBUTTONINFO message</span></span>

<span data-ttu-id="d68f6-105">Позволяет объекту обратного вызова добавлять кнопки на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="d68f6-105">Allows the callback object to add buttons to the toolbar.</span></span> <span data-ttu-id="d68f6-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="d68f6-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETBUTTONINFO 

    lParam = (LPARAM)(LPTBINFO) ptbinfo;

            
```



## <a name="parameters"></a><span data-ttu-id="d68f6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="d68f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d68f6-108">*птбинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="d68f6-108">*ptbinfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d68f6-109">Адрес структуры [**тбинфо**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) , указывающей количество кнопок и способ их добавления на панель инструментов.</span><span class="sxs-lookup"><span data-stu-id="d68f6-109">The address of a [**TBINFO**](/windows/desktop/api/Shlobj/ns-shlobj-tbinfo) structure that specifies the number of buttons and how they are to be added to the toolbar.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d68f6-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="d68f6-110">Remarks</span></span>

<span data-ttu-id="d68f6-111">Кнопки можно добавлять или добавлять в начало стандартных кнопок представления объектов в системных папках или отображаться вместо стандартных кнопок.</span><span class="sxs-lookup"><span data-stu-id="d68f6-111">Buttons can be appended or prepended to the standard system folder view object buttons, or be displayed in place of the standard buttons.</span></span> <span data-ttu-id="d68f6-112">За этим сообщением следует сообщение [**сфвм \_**](sfvm-getbuttons.md) , которое извлекает сведения о характере для кнопки.</span><span class="sxs-lookup"><span data-stu-id="d68f6-112">This message is followed by a [**SFVM\_GETBUTTONS**](sfvm-getbuttons.md) message that retrieves the information concerning the button specifics.</span></span>

## <a name="requirements"></a><span data-ttu-id="d68f6-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d68f6-113">Requirements</span></span>



| <span data-ttu-id="d68f6-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d68f6-114">Requirement</span></span> | <span data-ttu-id="d68f6-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d68f6-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d68f6-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d68f6-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d68f6-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d68f6-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="d68f6-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d68f6-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d68f6-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d68f6-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d68f6-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d68f6-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d68f6-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="d68f6-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
