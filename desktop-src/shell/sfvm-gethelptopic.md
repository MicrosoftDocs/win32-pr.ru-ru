---
description: 'Позволяет объекту обратного вызова указывать файл справки HTML и раздел внутри него. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_GETHELPTOPIC (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911396"
---
# <a name="sfvm_gethelptopic-message"></a><span data-ttu-id="ecfc9-104">\_Сообщение сфвм жеселптопик</span><span class="sxs-lookup"><span data-stu-id="ecfc9-104">SFVM\_GETHELPTOPIC message</span></span>

<span data-ttu-id="ecfc9-105">Позволяет объекту обратного вызова указывать файл справки HTML и раздел внутри него.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-105">Allows the callback object to specify an HTML Help file and a topic within it.</span></span> <span data-ttu-id="ecfc9-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="ecfc9-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a><span data-ttu-id="ecfc9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecfc9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecfc9-108">*ФТД* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ecfc9-108">*phtd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ecfc9-109">Адрес структуры [**\_ \_ данных сфвм хелптопик**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) , которая указывает файл справки HTML и раздел.</span><span class="sxs-lookup"><span data-stu-id="ecfc9-109">The address of a [**SFVM\_HELPTOPIC\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) structure that specifies the HTML Help file and topic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ecfc9-110">Требования</span><span class="sxs-lookup"><span data-stu-id="ecfc9-110">Requirements</span></span>



| <span data-ttu-id="ecfc9-111">Требование</span><span class="sxs-lookup"><span data-stu-id="ecfc9-111">Requirement</span></span> | <span data-ttu-id="ecfc9-112">Значение</span><span class="sxs-lookup"><span data-stu-id="ecfc9-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ecfc9-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecfc9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="ecfc9-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ecfc9-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="ecfc9-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecfc9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="ecfc9-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ecfc9-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="ecfc9-117">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ecfc9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecfc9-118"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecfc9-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
