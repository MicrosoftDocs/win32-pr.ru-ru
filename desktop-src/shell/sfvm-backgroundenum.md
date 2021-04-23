---
description: 'Позволяет объекту обратного вызова запрашивать перечисление в фоновом потоке. Используется Ишеллфолдервиевкб:: Мессажесфвкб.'
title: Сообщение SFVM_BACKGROUNDENUM (Шлобж. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 8428179c-2ec9-4979-9281-c2439e58beb6
api_name:
- SFVM_BACKGROUNDENUM
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: cb0b85abb3ca6830610a35502f55c0867a5ffbf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997827"
---
# <a name="sfvm_backgroundenum-message"></a><span data-ttu-id="66b28-104">\_Сообщение сфвм баккграунденум</span><span class="sxs-lookup"><span data-stu-id="66b28-104">SFVM\_BACKGROUNDENUM message</span></span>

<span data-ttu-id="66b28-105">Позволяет объекту обратного вызова запрашивать перечисление в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="66b28-105">Allows the callback object to request enumeration on a background thread.</span></span> <span data-ttu-id="66b28-106">Используется [**ишеллфолдервиевкб:: мессажесфвкб**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span><span class="sxs-lookup"><span data-stu-id="66b28-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++

                SFVM_BACKGROUNDENUM

            
```



## <a name="parameters"></a><span data-ttu-id="66b28-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="66b28-107">Parameters</span></span>

<span data-ttu-id="66b28-108">Это сообщение не содержит параметров.</span><span class="sxs-lookup"><span data-stu-id="66b28-108">This message has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="66b28-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="66b28-109">Remarks</span></span>

<span data-ttu-id="66b28-110">В ответ на это уведомление необходимо вернуть \_ значение ОК, чтобы включить перечисление фона.</span><span class="sxs-lookup"><span data-stu-id="66b28-110">In response to this notification, return S\_OK to enable background enumeration.</span></span> <span data-ttu-id="66b28-111">По умолчанию объект системной папки будет отображать анимацию "фонарик" во время перечисления.</span><span class="sxs-lookup"><span data-stu-id="66b28-111">By default, the system folder object will display the "flashlight" animation while the enumeration is taking place.</span></span> <span data-ttu-id="66b28-112">Чтобы задать пользовательскую анимацию, обработайте [**СФВМ \_ Animation**](sfvm-getanimation.md).</span><span class="sxs-lookup"><span data-stu-id="66b28-112">To specify a custom animation, handle [**SFVM\_GETANIMATION**](sfvm-getanimation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="66b28-113">Требования</span><span class="sxs-lookup"><span data-stu-id="66b28-113">Requirements</span></span>



| <span data-ttu-id="66b28-114">Требование</span><span class="sxs-lookup"><span data-stu-id="66b28-114">Requirement</span></span> | <span data-ttu-id="66b28-115">Значение</span><span class="sxs-lookup"><span data-stu-id="66b28-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="66b28-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66b28-116">Minimum supported client</span></span><br/> | <span data-ttu-id="66b28-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66b28-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="66b28-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66b28-118">Minimum supported server</span></span><br/> | <span data-ttu-id="66b28-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="66b28-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="66b28-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="66b28-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="66b28-121"><dt>Шлобж. h</dt></span><span class="sxs-lookup"><span data-stu-id="66b28-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
