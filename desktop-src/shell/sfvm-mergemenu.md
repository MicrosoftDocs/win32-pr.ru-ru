---
description: 'Позволяет объекту обратного вызова объединять пункты меню в меню проводника Windows. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_MERGEMENU (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104986076"
---
# <a name="sfvm_mergemenu-message"></a><span data-ttu-id="e005c-104">\_Сообщение сфвм мержемену</span><span class="sxs-lookup"><span data-stu-id="e005c-104">SFVM\_MERGEMENU message</span></span>

<span data-ttu-id="e005c-105">Позволяет объекту обратного вызова объединять пункты меню в меню проводника Windows.</span><span class="sxs-lookup"><span data-stu-id="e005c-105">Allows the callback object to merge menu items into the Windows Explorer menus.</span></span> <span data-ttu-id="e005c-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="e005c-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a><span data-ttu-id="e005c-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="e005c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e005c-108">*пинфо* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e005c-108">*pInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e005c-109">Структура [**ккминфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) , содержащая сведения, необходимые для слияния элементов в меню.</span><span class="sxs-lookup"><span data-stu-id="e005c-109">A [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information needed to merge the items into the menu.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e005c-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="e005c-110">Remarks</span></span>

<span data-ttu-id="e005c-111">Это сообщение, по сути, такое же самое, что и [**ишеллбровсер:: инсертменуссб**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) и [**Ишеллбровсер:: сетменусб**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) в представлении пользовательской папки.</span><span class="sxs-lookup"><span data-stu-id="e005c-111">This message serves essentially the same purpose as the [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) and [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in a custom folder view.</span></span> <span data-ttu-id="e005c-112">Дополнительные сведения см. в разделе *Использование ишеллбровсер для взаимодействия с проводником Windows* в статье [Реализация представления папки](../lwef/nse-folderview.md) .</span><span class="sxs-lookup"><span data-stu-id="e005c-112">See the *Using IShellBrowser to Communicate with Windows Explorer* section of [Implementing a Folder View](../lwef/nse-folderview.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="e005c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e005c-113">Requirements</span></span>



| <span data-ttu-id="e005c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="e005c-114">Requirement</span></span> | <span data-ttu-id="e005c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e005c-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e005c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e005c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e005c-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e005c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e005c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e005c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e005c-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e005c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e005c-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e005c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e005c-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="e005c-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
