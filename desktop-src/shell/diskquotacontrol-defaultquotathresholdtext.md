---
description: Возвращает пороговое значение квоты по умолчанию в виде текстовой строки.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Дисккуотаконтрол. Дефаулткуотасрешолдтекст, свойство
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143936"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a><span data-ttu-id="3e458-103">Дисккуотаконтрол. Дефаулткуотасрешолдтекст, свойство</span><span class="sxs-lookup"><span data-stu-id="3e458-103">DiskQuotaControl.DefaultQuotaThresholdText property</span></span>

<span data-ttu-id="3e458-104">Возвращает пороговое значение квоты по умолчанию в виде текстовой строки.</span><span class="sxs-lookup"><span data-stu-id="3e458-104">Gets the default quota threshold as a text string.</span></span>

<span data-ttu-id="3e458-105">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3e458-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e458-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e458-106">Syntax</span></span>


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="3e458-107">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3e458-107">Property value</span></span>

<span data-ttu-id="3e458-108">Строковое значение, содержащее порог квоты по умолчанию для тома.</span><span class="sxs-lookup"><span data-stu-id="3e458-108">A string value that contains the default quota threshold for the volume.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e458-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="3e458-109">Remarks</span></span>

<span data-ttu-id="3e458-110">Пороговое значение квоты по умолчанию применяется автоматически к новым пользователям тома.</span><span class="sxs-lookup"><span data-stu-id="3e458-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="3e458-111">Если использование диска пользователем превышает это значение, а свойство [**логкуотасрешолд**](diskquotacontrol-logquotathreshold.md) имеет значение **true**, система создает запись в журнале событий.</span><span class="sxs-lookup"><span data-stu-id="3e458-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="3e458-112">Например, если пороговое значение по умолчанию — 10,0 МБ, значение свойства равно "10,0 МБ".</span><span class="sxs-lookup"><span data-stu-id="3e458-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="3e458-113">Если для тома не задано пороговое значение по умолчанию, свойство имеет значение "без ограничений" или локализованный эквивалент.</span><span class="sxs-lookup"><span data-stu-id="3e458-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e458-114">Требования</span><span class="sxs-lookup"><span data-stu-id="3e458-114">Requirements</span></span>



| <span data-ttu-id="3e458-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3e458-115">Requirement</span></span> | <span data-ttu-id="3e458-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3e458-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e458-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e458-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e458-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3e458-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3e458-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e458-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e458-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3e458-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3e458-121">DLL</span><span class="sxs-lookup"><span data-stu-id="3e458-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e458-122"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="3e458-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e458-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e458-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e458-124">**дисккуотаконтрол**</span><span class="sxs-lookup"><span data-stu-id="3e458-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




