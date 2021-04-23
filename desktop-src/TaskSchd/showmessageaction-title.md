---
title: Шовмессажеактион. Title, свойство
description: Для создания скриптов Возвращает или задает заголовок окна сообщения.
ms.assetid: f61177fc-287c-4da9-9bdc-88aaa6868204
keywords:
- планировщик задач свойства Title
- Свойство Title планировщик задач, объект Шовмессажеактион
- Планировщик задач объекта Шовмессажеактион, свойство Title
topic_type:
- apiref
api_name:
- ShowMessageAction.Title
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2e552bb51653248e0a70ccfc0edea907749900e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801601"
---
# <a name="showmessageactiontitle-property"></a><span data-ttu-id="b4e23-106">Шовмессажеактион. Title, свойство</span><span class="sxs-lookup"><span data-stu-id="b4e23-106">ShowMessageAction.Title property</span></span>

<span data-ttu-id="b4e23-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b4e23-107">\[This object is no longer supported.</span></span> <span data-ttu-id="b4e23-108">Для отображения сообщения в сеансе пользователя можно использовать Иексекактион с функцией Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .\]</span><span class="sxs-lookup"><span data-stu-id="b4e23-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="b4e23-109">Для создания скриптов Возвращает или задает заголовок окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4e23-109">For scripting, gets or sets the title of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4e23-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b4e23-110">Syntax</span></span>


```VB
ShowMessageAction.Title As String
```



## <a name="property-value"></a><span data-ttu-id="b4e23-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b4e23-111">Property value</span></span>

<span data-ttu-id="b4e23-112">Название окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4e23-112">The title of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4e23-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b4e23-113">Remarks</span></span>

<span data-ttu-id="b4e23-114">Параметризованные строки можно использовать в тексте заголовка окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="b4e23-114">Parameterized strings can be used in the title text of the message box.</span></span> <span data-ttu-id="b4e23-115">Дополнительные сведения см. в разделе "примеры" в [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="b4e23-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="b4e23-116">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="b4e23-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="b4e23-117">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="b4e23-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="b4e23-118">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="b4e23-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="b4e23-119">Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="b4e23-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4e23-120">Требования</span><span class="sxs-lookup"><span data-stu-id="b4e23-120">Requirements</span></span>



| <span data-ttu-id="b4e23-121">Требование</span><span class="sxs-lookup"><span data-stu-id="b4e23-121">Requirement</span></span> | <span data-ttu-id="b4e23-122">Значение</span><span class="sxs-lookup"><span data-stu-id="b4e23-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b4e23-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b4e23-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b4e23-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b4e23-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="b4e23-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b4e23-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b4e23-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b4e23-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b4e23-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="b4e23-127">End of client support</span></span><br/>    | <span data-ttu-id="b4e23-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b4e23-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="b4e23-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="b4e23-129">End of server support</span></span><br/>    | <span data-ttu-id="b4e23-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="b4e23-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="b4e23-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="b4e23-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4e23-132"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="b4e23-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="b4e23-133">DLL</span><span class="sxs-lookup"><span data-stu-id="b4e23-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4e23-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4e23-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4e23-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b4e23-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4e23-136">**шовмессажеактион**</span><span class="sxs-lookup"><span data-stu-id="b4e23-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

