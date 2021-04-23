---
description: СФВМ \_ жетдетаилсоф может быть изменен или недоступен.
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: Сообщение SFVM_GETDETAILSOF (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104985769"
---
# <a name="sfvm_getdetailsof-message"></a><span data-ttu-id="c41c5-103">\_Сообщение сфвм жетдетаилсоф</span><span class="sxs-lookup"><span data-stu-id="c41c5-103">SFVM\_GETDETAILSOF message</span></span>

<span data-ttu-id="c41c5-104">\[**Сфвм \_ ЖЕТДЕТАИЛСОФ** доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="c41c5-104">\[**SFVM\_GETDETAILSOF** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c41c5-105">В последующих версиях он может быть изменен или недоступен.\]</span><span class="sxs-lookup"><span data-stu-id="c41c5-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="c41c5-106">Позволяет объекту обратного вызова предоставлять сведения для элемента в папке оболочки.</span><span class="sxs-lookup"><span data-stu-id="c41c5-106">Allows the callback object to provide the details for an item in a Shell folder.</span></span> <span data-ttu-id="c41c5-107">Используйте только в случае, если вызов [**IShellFolder2:: жетдетаилсоф**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) завершается с ошибкой и отсутствует доступный для вызова метод [**Ишеллдетаилс:: жетдетаилсоф**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) .</span><span class="sxs-lookup"><span data-stu-id="c41c5-107">Use only if a call to [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fails and there is no [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) method available to call.</span></span> <span data-ttu-id="c41c5-108">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="c41c5-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a><span data-ttu-id="c41c5-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="c41c5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c41c5-110">*иколумн* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="c41c5-110">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c41c5-111">Идентификатор столбца, начинающийся с нуля.</span><span class="sxs-lookup"><span data-stu-id="c41c5-111">The zero-based ID of the column.</span></span>

</dd> <dt>

<span data-ttu-id="c41c5-112">*ПДИ* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="c41c5-112">*pDi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c41c5-113">Указатель на структуру [**детаилсинфо**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) , заполненную запрошенной информацией.</span><span class="sxs-lookup"><span data-stu-id="c41c5-113">A pointer to a [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) structure filled with the requested information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c41c5-114">Требования</span><span class="sxs-lookup"><span data-stu-id="c41c5-114">Requirements</span></span>



| <span data-ttu-id="c41c5-115">Требование</span><span class="sxs-lookup"><span data-stu-id="c41c5-115">Requirement</span></span> | <span data-ttu-id="c41c5-116">Значение</span><span class="sxs-lookup"><span data-stu-id="c41c5-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c41c5-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c41c5-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c41c5-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="c41c5-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="c41c5-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c41c5-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c41c5-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="c41c5-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="c41c5-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="c41c5-121">End of client support</span></span><br/>    | <span data-ttu-id="c41c5-122">Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="c41c5-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="c41c5-123">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="c41c5-123">End of server support</span></span><br/>    | <span data-ttu-id="c41c5-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c41c5-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="c41c5-125">Header</span><span class="sxs-lookup"><span data-stu-id="c41c5-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="c41c5-126"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="c41c5-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
