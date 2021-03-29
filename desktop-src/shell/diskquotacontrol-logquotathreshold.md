---
description: Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем порога назначенной квоты.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Дисккуотаконтрол. Логкуотасрешолд, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984244"
---
# <a name="diskquotacontrollogquotathreshold-property"></a><span data-ttu-id="5335f-103">Дисккуотаконтрол. Логкуотасрешолд, свойство</span><span class="sxs-lookup"><span data-stu-id="5335f-103">DiskQuotaControl.LogQuotaThreshold property</span></span>

<span data-ttu-id="5335f-104">Задает или возвращает логическое значение, указывающее, будет ли выполняться запись в журнале системных событий при превышении пользователем порога назначенной квоты.</span><span class="sxs-lookup"><span data-stu-id="5335f-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span>

<span data-ttu-id="5335f-105">Это свойство доступно для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="5335f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5335f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5335f-106">Syntax</span></span>


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="5335f-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5335f-107">Property value</span></span>

<span data-ttu-id="5335f-108">Это свойство имеет значение **true** , если запись журнала системных событий выполняется при превышении пользователем порога предупреждения квоты или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5335f-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota warning threshold, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="5335f-109">Требования</span><span class="sxs-lookup"><span data-stu-id="5335f-109">Requirements</span></span>



| <span data-ttu-id="5335f-110">Требование</span><span class="sxs-lookup"><span data-stu-id="5335f-110">Requirement</span></span> | <span data-ttu-id="5335f-111">Значение</span><span class="sxs-lookup"><span data-stu-id="5335f-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5335f-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5335f-112">Minimum supported client</span></span><br/> | <span data-ttu-id="5335f-113">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5335f-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5335f-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5335f-114">Minimum supported server</span></span><br/> | <span data-ttu-id="5335f-115">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="5335f-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="5335f-116">DLL</span><span class="sxs-lookup"><span data-stu-id="5335f-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5335f-117"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="5335f-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5335f-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="5335f-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5335f-119">**дефаулткуотасрешолд**</span><span class="sxs-lookup"><span data-stu-id="5335f-119">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="5335f-120">**Объект Дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="5335f-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="5335f-121">**логкуоталимит**</span><span class="sxs-lookup"><span data-stu-id="5335f-121">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




