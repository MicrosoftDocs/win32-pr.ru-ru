---
title: Свойство Principal. DisplayName
description: Для создания скриптов Возвращает или задает имя участника.
ms.assetid: 73caf263-f597-4bea-ae89-32f9919d7a70
keywords:
- планировщик задач свойства DisplayName
- Свойство DisplayName планировщик задач, объект Principal
- Объект Principal планировщик задач, свойство DisplayName
topic_type:
- apiref
api_name:
- Principal.DisplayName
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31a76ec9473bccb20ec484259ab8adfe26ad6441
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802555"
---
# <a name="principaldisplayname-property"></a><span data-ttu-id="fac17-106">Свойство Principal. DisplayName</span><span class="sxs-lookup"><span data-stu-id="fac17-106">Principal.DisplayName property</span></span>

<span data-ttu-id="fac17-107">Для создания скриптов Возвращает или задает имя участника.</span><span class="sxs-lookup"><span data-stu-id="fac17-107">For scripting, gets or sets the name of the principal..</span></span>

## <a name="syntax"></a><span data-ttu-id="fac17-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fac17-108">Syntax</span></span>


```VB
Principal.DisplayName As String
```



## <a name="property-value"></a><span data-ttu-id="fac17-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fac17-109">Property value</span></span>

<span data-ttu-id="fac17-110">Имя участника.</span><span class="sxs-lookup"><span data-stu-id="fac17-110">The name of the principal.</span></span>

## <a name="remarks"></a><span data-ttu-id="fac17-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fac17-111">Remarks</span></span>

<span data-ttu-id="fac17-112">При чтении или записи XML для задачи отображаемое имя участника указывается в элементе [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) схемы планировщик задач.</span><span class="sxs-lookup"><span data-stu-id="fac17-112">When reading or writing XML for a task, the display name for a principal is specified in the [**DisplayName**](taskschedulerschema-displayname-principaltype-element.md) element of the Task Scheduler schema.</span></span>

<span data-ttu-id="fac17-113">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="fac17-113">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="fac17-114">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="fac17-114">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="fac17-115">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="fac17-115">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="fac17-116">Например, если задать для этого свойства значение $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101), в файле% SystemRoot% System32ResourceName.dll будет задано значение для свойства, равное-101 \\ \\ .</span><span class="sxs-lookup"><span data-stu-id="fac17-116">For example, setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="fac17-117">Требования</span><span class="sxs-lookup"><span data-stu-id="fac17-117">Requirements</span></span>



| <span data-ttu-id="fac17-118">Требование</span><span class="sxs-lookup"><span data-stu-id="fac17-118">Requirement</span></span> | <span data-ttu-id="fac17-119">Значение</span><span class="sxs-lookup"><span data-stu-id="fac17-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fac17-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fac17-120">Minimum supported client</span></span><br/> | <span data-ttu-id="fac17-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fac17-121">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="fac17-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fac17-122">Minimum supported server</span></span><br/> | <span data-ttu-id="fac17-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fac17-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fac17-124">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="fac17-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="fac17-125"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="fac17-125"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="fac17-126">DLL</span><span class="sxs-lookup"><span data-stu-id="fac17-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac17-127"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac17-127"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac17-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fac17-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac17-129">Планировщик заданий</span><span class="sxs-lookup"><span data-stu-id="fac17-129">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> <dt>

[<span data-ttu-id="fac17-130">**Основного**</span><span class="sxs-lookup"><span data-stu-id="fac17-130">**Principal**</span></span>](principal.md)
</dt> </dl>

 

 





