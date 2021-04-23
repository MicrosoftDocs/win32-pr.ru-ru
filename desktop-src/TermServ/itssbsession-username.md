---
title: Свойство UserName Итссбсессион
description: Возвращает имя пользователя для этого сеанса.
ms.assetid: 0034e8cc-b67b-4e30-a059-47a269bab0fd
ms.tgt_platform: multiple
keywords:
- службы удаленных рабочих столов свойства имени пользователя
- Свойство UserName службы удаленных рабочих столов, интерфейс Итссбсессион
- Службы удаленных рабочих столов интерфейса Итссбсессион, свойство UserName
topic_type:
- apiref
api_name:
- ITsSbSession.Username
- ITsSbSession.get_Username
api_location:
- Sbtsv.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fb66f0639d659fcb6800680ffc3b3486ad12b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672878"
---
# <a name="itssbsessionusername-property"></a><span data-ttu-id="c69b1-106">Свойство Итссбсессион:: username</span><span class="sxs-lookup"><span data-stu-id="c69b1-106">ITsSbSession::Username property</span></span>

<span data-ttu-id="c69b1-107">Возвращает имя пользователя для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="c69b1-107">Retrieves the user name for this session.</span></span>

<span data-ttu-id="c69b1-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="c69b1-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c69b1-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c69b1-109">Syntax</span></span>


```C++
HRESULT get_Username(
  [out, retval] BSTR *userName
);
```



## <a name="property-value"></a><span data-ttu-id="c69b1-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="c69b1-110">Property value</span></span>

<span data-ttu-id="c69b1-111">Указатель на переменную **BSTR** , которая получает имя пользователя для этого сеанса.</span><span class="sxs-lookup"><span data-stu-id="c69b1-111">A pointer to a **BSTR** variable that receives the user name for this session.</span></span>

## <a name="requirements"></a><span data-ttu-id="c69b1-112">Требования</span><span class="sxs-lookup"><span data-stu-id="c69b1-112">Requirements</span></span>



| <span data-ttu-id="c69b1-113">Требование</span><span class="sxs-lookup"><span data-stu-id="c69b1-113">Requirement</span></span> | <span data-ttu-id="c69b1-114">Значение</span><span class="sxs-lookup"><span data-stu-id="c69b1-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="c69b1-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c69b1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c69b1-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="c69b1-116">None supported</span></span><br/>                                                            |
| <span data-ttu-id="c69b1-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c69b1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c69b1-118">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c69b1-118">Windows Server 2012</span></span><br/>                                                       |
| <span data-ttu-id="c69b1-119">IDL</span><span class="sxs-lookup"><span data-stu-id="c69b1-119">IDL</span></span><br/>                      | <dl> <span data-ttu-id="c69b1-120"><dt>Сбтсв. idl</dt></span><span class="sxs-lookup"><span data-stu-id="c69b1-120"><dt>Sbtsv.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c69b1-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c69b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c69b1-122">**итссбсессион**</span><span class="sxs-lookup"><span data-stu-id="c69b1-122">**ITsSbSession**</span></span>](/windows/desktop/api/sbtsv/nn-sbtsv-itssbsession)
</dt> </dl>

 

 





