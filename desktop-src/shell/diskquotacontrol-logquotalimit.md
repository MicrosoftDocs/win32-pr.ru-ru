---
description: Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем назначенной квоты.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Дисккуотаконтрол. Логкуоталимит, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984245"
---
# <a name="diskquotacontrollogquotalimit-property"></a><span data-ttu-id="48962-103">Дисккуотаконтрол. Логкуоталимит, свойство</span><span class="sxs-lookup"><span data-stu-id="48962-103">DiskQuotaControl.LogQuotaLimit property</span></span>

<span data-ttu-id="48962-104">Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем назначенной квоты.</span><span class="sxs-lookup"><span data-stu-id="48962-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span>

<span data-ttu-id="48962-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="48962-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="48962-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48962-106">Syntax</span></span>


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="48962-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="48962-107">Property value</span></span>

<span data-ttu-id="48962-108">Это свойство имеет значение **true** , если запись в журнале системных событий выполняется при превышении пользователем предела квоты или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="48962-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota limit, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="48962-109">Требования</span><span class="sxs-lookup"><span data-stu-id="48962-109">Requirements</span></span>



| <span data-ttu-id="48962-110">Требование</span><span class="sxs-lookup"><span data-stu-id="48962-110">Requirement</span></span> | <span data-ttu-id="48962-111">Значение</span><span class="sxs-lookup"><span data-stu-id="48962-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48962-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48962-112">Minimum supported client</span></span><br/> | <span data-ttu-id="48962-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="48962-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="48962-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48962-114">Minimum supported server</span></span><br/> | <span data-ttu-id="48962-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="48962-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="48962-116">DLL</span><span class="sxs-lookup"><span data-stu-id="48962-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48962-117"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="48962-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48962-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48962-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48962-119">**дефаулткуоталимит**</span><span class="sxs-lookup"><span data-stu-id="48962-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="48962-120">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="48962-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="48962-121">**логкуотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="48962-121">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




