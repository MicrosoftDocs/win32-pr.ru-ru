---
title: Перечисление Вмстартупоптион (Впккоминтерфацес. h)
description: Указывает параметр запуска.
ms.assetid: ac4de9a7-7fc7-4361-89dd-e7da8f5dbb92
keywords:
- Перечисление Вмстартупоптион Virtual PC
topic_type:
- apiref
api_name:
- VMStartupOption
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dc4a3bbcc1c82c57dfe144f818c29b403fd83a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490431"
---
# <a name="vmstartupoption-enumeration"></a><span data-ttu-id="ce0e2-104">Перечисление Вмстартупоптион</span><span class="sxs-lookup"><span data-stu-id="ce0e2-104">VMStartupOption enumeration</span></span>

<span data-ttu-id="ce0e2-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ce0e2-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ce0e2-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ce0e2-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ce0e2-107">Указывает параметр запуска.</span><span class="sxs-lookup"><span data-stu-id="ce0e2-107">Specifies the start-up option.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce0e2-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce0e2-108">Syntax</span></span>


```C++
typedef enum  { 
  vmStartupOption_Normal                      = 0,
  vmStartupOption_FixParentTimestampMismatch  = 1
} VMStartupOption;
```



## <a name="constants"></a><span data-ttu-id="ce0e2-109">Константы</span><span class="sxs-lookup"><span data-stu-id="ce0e2-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce0e2-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**Вмстартупоптион, \_ Обычная**</span><span class="sxs-lookup"><span data-stu-id="ce0e2-110"><span id="vmStartupOption_Normal"></span><span id="vmstartupoption_normal"></span><span id="VMSTARTUPOPTION_NORMAL"></span>**vmStartupOption\_Normal**</span></span>
</dt> <dd>

<span data-ttu-id="ce0e2-111">Запуск в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="ce0e2-111">Start normally.</span></span>

</dd> <dt>

<span data-ttu-id="ce0e2-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**Вмстартупоптион \_ фикспаренттиместампмисматч**</span><span class="sxs-lookup"><span data-stu-id="ce0e2-112"><span id="vmStartupOption_FixParentTimestampMismatch"></span><span id="vmstartupoption_fixparenttimestampmismatch"></span><span id="VMSTARTUPOPTION_FIXPARENTTIMESTAMPMISMATCH"></span>**vmStartupOption\_FixParentTimestampMismatch**</span></span>
</dt> <dd>

<span data-ttu-id="ce0e2-113">Исправьте несоответствие родительской метки времени.</span><span class="sxs-lookup"><span data-stu-id="ce0e2-113">Fix the parent timestamp mismatch.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce0e2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="ce0e2-114">Requirements</span></span>



| <span data-ttu-id="ce0e2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="ce0e2-115">Requirement</span></span> | <span data-ttu-id="ce0e2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="ce0e2-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0e2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce0e2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ce0e2-118">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ce0e2-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce0e2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce0e2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ce0e2-120">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ce0e2-120">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ce0e2-121">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="ce0e2-121">End of client support</span></span><br/>    | <span data-ttu-id="ce0e2-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce0e2-122">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ce0e2-123">Продукт</span><span class="sxs-lookup"><span data-stu-id="ce0e2-123">Product</span></span><br/>                  | <span data-ttu-id="ce0e2-124">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ce0e2-124">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ce0e2-125">Header</span><span class="sxs-lookup"><span data-stu-id="ce0e2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce0e2-126"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce0e2-126"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce0e2-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce0e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce0e2-128">**Ивмвиртуалмачине:: Startup2**</span><span class="sxs-lookup"><span data-stu-id="ce0e2-128">**IVMVirtualMachine::Startup2**</span></span>](ivmvirtualmachine-startup2.md)
</dt> </dl>

 

