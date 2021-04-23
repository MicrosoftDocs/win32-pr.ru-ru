---
title: Регистратионинфо. SecurityDescriptor, свойство
description: Для создания скриптов Возвращает или задает дескриптор безопасности задачи.
ms.assetid: e03607f0-c2a0-4aa1-a2b0-915b03aae968
keywords:
- планировщик задач свойства SecurityDescriptor
- Планировщик задач свойства SecurityDescriptor, объект Регистратионинфо
- Планировщик задач объекта Регистратионинфо, свойство SecurityDescriptor
topic_type:
- apiref
api_name:
- RegistrationInfo.SecurityDescriptor
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 379e42f41387a40b160a73ec3457d3d5b9feaf59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105681746"
---
# <a name="registrationinfosecuritydescriptor-property"></a><span data-ttu-id="fb32b-106">Регистратионинфо. SecurityDescriptor, свойство</span><span class="sxs-lookup"><span data-stu-id="fb32b-106">RegistrationInfo.SecurityDescriptor property</span></span>

<span data-ttu-id="fb32b-107">Для создания скриптов Возвращает или задает дескриптор безопасности задачи.</span><span class="sxs-lookup"><span data-stu-id="fb32b-107">For scripting, gets or sets the security descriptor of the task.</span></span> <span data-ttu-id="fb32b-108">Если во время регистрации задачи был указан другой дескриптор безопасности, он заменит дескриптор безопасности, установленный этим свойством.</span><span class="sxs-lookup"><span data-stu-id="fb32b-108">If a different security descriptor is supplied during task registration, it will supersede the security descriptor set with this property.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb32b-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb32b-109">Syntax</span></span>


```VB
RegistrationInfo.SecurityDescriptor As String
```



## <a name="property-value"></a><span data-ttu-id="fb32b-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fb32b-110">Property value</span></span>

<span data-ttu-id="fb32b-111">Дескриптор безопасности, связанный с задачей.</span><span class="sxs-lookup"><span data-stu-id="fb32b-111">The security descriptor that is associated with the task.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb32b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb32b-112">Remarks</span></span>

<span data-ttu-id="fb32b-113">При чтении или записи XML-кода для задачи дескриптор безопасности задачи указывается с помощью элемента [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="fb32b-113">When reading or writing XML for a task, the security descriptor of the task is specified using the [**SecurityDescriptor**](taskschedulerschema-securitydescriptor-registrationinfotype-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb32b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="fb32b-114">Requirements</span></span>



| <span data-ttu-id="fb32b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="fb32b-115">Requirement</span></span> | <span data-ttu-id="fb32b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fb32b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb32b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fb32b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fb32b-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fb32b-118">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fb32b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fb32b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fb32b-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fb32b-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb32b-121">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fb32b-121">Type library</span></span><br/>             | <dl> <span data-ttu-id="fb32b-122"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fb32b-122"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fb32b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="fb32b-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb32b-124"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb32b-124"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb32b-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb32b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb32b-126">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fb32b-126">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





