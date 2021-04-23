---
title: Шовмессажеактион. MessageBody, свойство
description: Для создания скриптов Возвращает или задает текст сообщения, отображаемого в тексте окна сообщения.
ms.assetid: 7166e379-95f0-43f1-93a0-6a3d706dd627
keywords:
- планировщик задач свойства MessageBody
- Планировщик задач свойства MessageBody, объект Шовмессажеактион
- Планировщик задач объекта Шовмессажеактион, свойство MessageBody
topic_type:
- apiref
api_name:
- ShowMessageAction.MessageBody
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1604367a8daad1ae1b5f44c6021d22bf1aa7c5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103891613"
---
# <a name="showmessageactionmessagebody-property"></a><span data-ttu-id="e2701-106">Шовмессажеактион. MessageBody, свойство</span><span class="sxs-lookup"><span data-stu-id="e2701-106">ShowMessageAction.MessageBody property</span></span>

<span data-ttu-id="e2701-107">\[Этот объект больше не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="e2701-107">\[This object is no longer supported.</span></span> <span data-ttu-id="e2701-108">Для отображения сообщения в сеансе пользователя можно использовать Иексекактион с функцией Windows Scripting [**MsgBox**](/previous-versions/sfw6660x(v=vs.80)) .\]</span><span class="sxs-lookup"><span data-stu-id="e2701-108">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.\]</span></span>

<span data-ttu-id="e2701-109">Для создания скриптов Возвращает или задает текст сообщения, отображаемого в тексте окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2701-109">For scripting, gets or sets the message text that is displayed in the body of the message box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2701-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e2701-110">Syntax</span></span>


```VB
ShowMessageAction.MessageBody As String
```



## <a name="property-value"></a><span data-ttu-id="e2701-111">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e2701-111">Property value</span></span>

<span data-ttu-id="e2701-112">Текст сообщения, отображаемый в тексте окна сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2701-112">The message text that is displayed in the body of the message box.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2701-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e2701-113">Remarks</span></span>

<span data-ttu-id="e2701-114">Параметризованные строки можно использовать в тексте сообщения в окне сообщения.</span><span class="sxs-lookup"><span data-stu-id="e2701-114">Parameterized strings can be used in the message text of the message box.</span></span> <span data-ttu-id="e2701-115">Дополнительные сведения см. в разделе "примеры" в [**EventTrigger. валуекуериес**](eventtrigger-valuequeries.md).</span><span class="sxs-lookup"><span data-stu-id="e2701-115">For more information, see the Examples section in [**EventTrigger.ValueQueries**](eventtrigger-valuequeries.md).</span></span>

<span data-ttu-id="e2701-116">При задании значения этого свойства значением может быть текст, полученный из файла resource. dll.</span><span class="sxs-lookup"><span data-stu-id="e2701-116">When setting this property value, the value can be text that is retrieved from a resource .dll file.</span></span> <span data-ttu-id="e2701-117">Для ссылки на текст из файла ресурсов используется специализированная строка.</span><span class="sxs-lookup"><span data-stu-id="e2701-117">A specialized string is used to reference the text from the resource file.</span></span> <span data-ttu-id="e2701-118">Строка имеет формат $ (@ \[ DLL \] , \[ ResourceId \] ), где \[ DLL — это \] путь к DLL-файлу, содержащему ресурс, а \[ ResourceId \] — идентификатор для текста ресурса.</span><span class="sxs-lookup"><span data-stu-id="e2701-118">The format of the string is $(@ \[Dll\], \[ResourceID\]) where \[Dll\] is the path to the .dll file that contains the resource and \[ResourceID\] is the identifier for the resource text.</span></span> <span data-ttu-id="e2701-119">Например, при установке значения этого свойства в $ (@% SystemRoot% \\ System32 \\ResourceName.dll,-101) свойству будет присвоено значение текста ресурса с идентификатором, равным-101, в файле% SystemRoot% \\ system32 \\ResourceName.dll.</span><span class="sxs-lookup"><span data-stu-id="e2701-119">For example, the setting this property value to $(@ %SystemRoot%\\System32\\ResourceName.dll, -101) will set the property to the value of the resource text with an identifier equal to -101 in the %SystemRoot%\\System32\\ResourceName.dll file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2701-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e2701-120">Requirements</span></span>



| <span data-ttu-id="e2701-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e2701-121">Requirement</span></span> | <span data-ttu-id="e2701-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e2701-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e2701-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e2701-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e2701-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e2701-124">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e2701-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e2701-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e2701-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e2701-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e2701-127">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="e2701-127">End of client support</span></span><br/>    | <span data-ttu-id="e2701-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e2701-128">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="e2701-129">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="e2701-129">End of server support</span></span><br/>    | <span data-ttu-id="e2701-130">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e2701-130">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e2701-131">Библиотека типов</span><span class="sxs-lookup"><span data-stu-id="e2701-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="e2701-132"><dt>Тасксчд. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="e2701-132"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="e2701-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e2701-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2701-134"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2701-134"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2701-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e2701-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2701-136">**шовмессажеактион**</span><span class="sxs-lookup"><span data-stu-id="e2701-136">**ShowMessageAction**</span></span>](showmessageaction.md)
</dt> </dl>

 

