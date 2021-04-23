---
description: 'Уведомляет объект обратного вызова о том, что пользователь щелкнул заголовок столбца, чтобы отсортировать список объектов в представлении папки. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_COLUMNCLICK (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104497889"
---
# <a name="sfvm_columnclick-message"></a><span data-ttu-id="57ed2-104">\_Сообщение сфвм колумнкликк</span><span class="sxs-lookup"><span data-stu-id="57ed2-104">SFVM\_COLUMNCLICK message</span></span>

<span data-ttu-id="57ed2-105">Уведомляет объект обратного вызова о том, что пользователь щелкнул заголовок столбца, чтобы отсортировать список объектов в представлении папки.</span><span class="sxs-lookup"><span data-stu-id="57ed2-105">Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</span></span> <span data-ttu-id="57ed2-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="57ed2-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="57ed2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="57ed2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57ed2-108">*иколумн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="57ed2-108">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57ed2-109">Индекс столбца, который был выбран.</span><span class="sxs-lookup"><span data-stu-id="57ed2-109">The index of the column that was clicked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="57ed2-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="57ed2-110">Remarks</span></span>

<span data-ttu-id="57ed2-111">В ответ на это уведомление следует вернуть \_ "ОК" для самостоятельного изменения списка.</span><span class="sxs-lookup"><span data-stu-id="57ed2-111">In response to this notification, you should return S\_OK to rearrange the list yourself.</span></span> <span data-ttu-id="57ed2-112">Чтобы объект представления системной папки переупорядочивает список, возвратите \_ значение false.</span><span class="sxs-lookup"><span data-stu-id="57ed2-112">To have the system folder view object rearrange the list, return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ed2-113">Требования</span><span class="sxs-lookup"><span data-stu-id="57ed2-113">Requirements</span></span>



| <span data-ttu-id="57ed2-114">Требование</span><span class="sxs-lookup"><span data-stu-id="57ed2-114">Requirement</span></span> | <span data-ttu-id="57ed2-115">Значение</span><span class="sxs-lookup"><span data-stu-id="57ed2-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="57ed2-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="57ed2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="57ed2-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57ed2-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="57ed2-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="57ed2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="57ed2-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="57ed2-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="57ed2-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="57ed2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ed2-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="57ed2-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
