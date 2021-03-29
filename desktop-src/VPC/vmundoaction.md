---
title: Перечисление Вмундоактион (Впккоминтерфацес. h)
description: Указывает, что произойдет для отмены дисков при выключении или отключении виртуальной машины.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Перечисление Вмундоактион Virtual PC
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535291"
---
# <a name="vmundoaction-enumeration"></a><span data-ttu-id="b54f1-104">Перечисление Вмундоактион</span><span class="sxs-lookup"><span data-stu-id="b54f1-104">VMUndoAction enumeration</span></span>

<span data-ttu-id="b54f1-105">\[Windows Virtual PC больше не доступна для использования в Windows 8.</span><span class="sxs-lookup"><span data-stu-id="b54f1-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b54f1-106">Вместо этого используйте [поставщик WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b54f1-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b54f1-107">Указывает, что произойдет для отмены дисков при выключении или отключении виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b54f1-107">Specifies what happens to undo drives when a virtual machine is shut down or turned off.</span></span>

## <a name="syntax"></a><span data-ttu-id="b54f1-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b54f1-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a><span data-ttu-id="b54f1-109">Константы</span><span class="sxs-lookup"><span data-stu-id="b54f1-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b54f1-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**Вмундоактион \_ отбросить**</span><span class="sxs-lookup"><span data-stu-id="b54f1-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction\_Discard**</span></span>
</dt> <dd>

<span data-ttu-id="b54f1-111">Отменить диски отмены; родительские диски остаются без изменений.</span><span class="sxs-lookup"><span data-stu-id="b54f1-111">Discard the undo drives; the parent drives remain unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="b54f1-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**Вмундоактион \_**</span><span class="sxs-lookup"><span data-stu-id="b54f1-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction\_Keep**</span></span>
</dt> <dd>

<span data-ttu-id="b54f1-113">Не отключайте диски отмены. родительские диски остаются без изменений, но изменения будут поддерживаться при следующем запуске виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="b54f1-113">Keep the undo drives; the parent drives remain unchanged, but changes will be maintained the next time the virtual machine starts.</span></span>

</dd> <dt>

<span data-ttu-id="b54f1-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**Вмундоактион \_ фиксация**</span><span class="sxs-lookup"><span data-stu-id="b54f1-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction\_Commit**</span></span>
</dt> <dd>

<span data-ttu-id="b54f1-115">Зафиксируйте изменения на родительских дисках.</span><span class="sxs-lookup"><span data-stu-id="b54f1-115">Commit changes to the parent drives.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b54f1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="b54f1-116">Requirements</span></span>



| <span data-ttu-id="b54f1-117">Требование</span><span class="sxs-lookup"><span data-stu-id="b54f1-117">Requirement</span></span> | <span data-ttu-id="b54f1-118">Значение</span><span class="sxs-lookup"><span data-stu-id="b54f1-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b54f1-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b54f1-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b54f1-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="b54f1-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b54f1-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b54f1-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b54f1-122">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b54f1-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b54f1-123">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b54f1-123">End of client support</span></span><br/>    | <span data-ttu-id="b54f1-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b54f1-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b54f1-125">Продукт</span><span class="sxs-lookup"><span data-stu-id="b54f1-125">Product</span></span><br/>                  | <span data-ttu-id="b54f1-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b54f1-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b54f1-127">Header</span><span class="sxs-lookup"><span data-stu-id="b54f1-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b54f1-128"><dt>Впккоминтерфацес. h</dt></span><span class="sxs-lookup"><span data-stu-id="b54f1-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b54f1-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b54f1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b54f1-130">**Ивмвиртуалмачине:: Ундоактион**</span><span class="sxs-lookup"><span data-stu-id="b54f1-130">**IVMVirtualMachine::UndoAction**</span></span>](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

