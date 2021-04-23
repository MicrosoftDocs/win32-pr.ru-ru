---
title: Итссбсессион Инитиалпрограм, свойство
description: Возвращает или задает начальную программу для данного сеанса.
ms.assetid: c299c4f7-3c5f-468f-9fc7-81eac322dfa2
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства Инитиалпрограм
- Службы удаленных рабочих столов свойства Инитиалпрограм, интерфейс Итссбсессион
- Службы удаленных рабочих столов интерфейса Итссбсессион, свойство Инитиалпрограм
topic_type:
- apiref
api_name:
- ITsSbSession.InitialProgram
- ITsSbSession.get_InitialProgram
- ITsSbSession.put_InitialProgram
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 307f8bb4330caf4b84b8650c9ccc2551c94da76d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490620"
---
# <a name="itssbsessioninitialprogram-property"></a><span data-ttu-id="9c92e-106">Свойство Итссбсессион:: Инитиалпрограм</span><span class="sxs-lookup"><span data-stu-id="9c92e-106">ITsSbSession::InitialProgram property</span></span>

<span data-ttu-id="9c92e-107">Возвращает или задает начальную программу для данного сеанса.</span><span class="sxs-lookup"><span data-stu-id="9c92e-107">Retrieves or specifies the initial program for this session.</span></span> <span data-ttu-id="9c92e-108">Начальная программа — это программа, которая запускается при запуске сеанса пользователя.</span><span class="sxs-lookup"><span data-stu-id="9c92e-108">The initial program is the program that is launched when the user session starts.</span></span>

<span data-ttu-id="9c92e-109">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="9c92e-109">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c92e-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9c92e-110">Syntax</span></span>


```C++
HRESULT put_InitialProgram(
  [in]          BSTR Application
);

HRESULT get_InitialProgram(
  [out, retval] BSTR *app
);
```



## <a name="property-value"></a><span data-ttu-id="9c92e-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9c92e-111">Property value</span></span>

<span data-ttu-id="9c92e-112">Переменная **BSTR** , содержащая начальную программу.</span><span class="sxs-lookup"><span data-stu-id="9c92e-112">A **BSTR** variable that contains the initial program.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c92e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="9c92e-113">Requirements</span></span>



| <span data-ttu-id="9c92e-114">Требование</span><span class="sxs-lookup"><span data-stu-id="9c92e-114">Requirement</span></span> | <span data-ttu-id="9c92e-115">Значение</span><span class="sxs-lookup"><span data-stu-id="9c92e-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9c92e-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9c92e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9c92e-117">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="9c92e-117">None supported</span></span><br/>                                                            |
| <span data-ttu-id="9c92e-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9c92e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9c92e-119">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="9c92e-119">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="9c92e-120">IDL</span><span class="sxs-lookup"><span data-stu-id="9c92e-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9c92e-121"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9c92e-121"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9c92e-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9c92e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c92e-123">**итссбсессион**</span><span class="sxs-lookup"><span data-stu-id="9c92e-123">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





