---
title: Тфгуидатом (Мсктф. h)
description: Тип данных Тфгуидатом определяет идентификатор GUID в TSF. Тфгуидатом получается путем вызова Итфкатегоримгр Регистергуид.
ms.assetid: 91696612-1829-4052-81d1-eddc23278d35
keywords:
- тфгуидатом
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c05d3c9a3bc7d725bf2df38069d7bc6112dad08b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135062"
---
# <a name="tfguidatom"></a><span data-ttu-id="6fd1d-105">тфгуидатом</span><span class="sxs-lookup"><span data-stu-id="6fd1d-105">TfGuidAtom</span></span>

<span data-ttu-id="6fd1d-106">Тип данных **тфгуидатом** определяет **идентификатор GUID** в TSF.</span><span class="sxs-lookup"><span data-stu-id="6fd1d-106">The **TfGuidAtom** data type identifies a **GUID** within TSF.</span></span> <span data-ttu-id="6fd1d-107">**Тфгуидатом** получается путем вызова [**Итфкатегоримгр:: регистергуид**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span><span class="sxs-lookup"><span data-stu-id="6fd1d-107">A **TfGuidAtom** is obtained by calling [**ITfCategoryMgr::RegisterGUID**](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid).</span></span>


```C++
typedef DWORD TfGuidAtom;
```



## <a name="remarks"></a><span data-ttu-id="6fd1d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6fd1d-108">Remarks</span></span>

<span data-ttu-id="6fd1d-109">Значение **тфгуидатом** допустимо только в пределах процесса, из которого вызывается **Итфкатегоримгр:: регистергуид** .</span><span class="sxs-lookup"><span data-stu-id="6fd1d-109">A **TfGuidAtom** value is only valid within the process that **ITfCategoryMgr::RegisterGUID** is called from.</span></span>

## <a name="requirements"></a><span data-ttu-id="6fd1d-110">Требования</span><span class="sxs-lookup"><span data-stu-id="6fd1d-110">Requirements</span></span>



| <span data-ttu-id="6fd1d-111">Требование</span><span class="sxs-lookup"><span data-stu-id="6fd1d-111">Requirement</span></span> | <span data-ttu-id="6fd1d-112">Значение</span><span class="sxs-lookup"><span data-stu-id="6fd1d-112">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6fd1d-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6fd1d-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6fd1d-114">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fd1d-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="6fd1d-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6fd1d-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6fd1d-116">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6fd1d-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6fd1d-117">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="6fd1d-117">Redistributable</span></span><br/>          | <span data-ttu-id="6fd1d-118">TSF 1,0 в Windows 2000 профессиональная</span><span class="sxs-lookup"><span data-stu-id="6fd1d-118">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                      |
| <span data-ttu-id="6fd1d-119">Header</span><span class="sxs-lookup"><span data-stu-id="6fd1d-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fd1d-120"><dt>Мсктф. h</dt></span><span class="sxs-lookup"><span data-stu-id="6fd1d-120"><dt>Msctf.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fd1d-121">IDL</span><span class="sxs-lookup"><span data-stu-id="6fd1d-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6fd1d-122"><dt>Мсктф. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6fd1d-122"><dt>Msctf.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fd1d-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6fd1d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fd1d-124">**Итфкатегоримгр:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="6fd1d-124">**ITfCategoryMgr::GetGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-getguid)
</dt> <dt>

[<span data-ttu-id="6fd1d-125">**Итфкатегоримгр:: Исекуалтфгуидатом**</span><span class="sxs-lookup"><span data-stu-id="6fd1d-125">**ITfCategoryMgr::IsEqualTfGuidAtom**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-isequaltfguidatom)
</dt> <dt>

[<span data-ttu-id="6fd1d-126">**Итфкатегоримгр:: Регистергуид**</span><span class="sxs-lookup"><span data-stu-id="6fd1d-126">**ITfCategoryMgr::RegisterGUID**</span></span>](/windows/desktop/api/Msctf/nf-msctf-itfcategorymgr-registerguid)
</dt> </dl>

 

 





