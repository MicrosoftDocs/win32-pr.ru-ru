---
description: Указывает, что объект Шеллфолдервиев завершил перечисление содержимого папки.
title: Событие Шеллфолдервиевок. Енумдоне (Шлдисп. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnumDone
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 7baa5f58-62c2-406e-a81e-4ca9c446a756
ms.openlocfilehash: 00b0e58ed18ab0da9c3fa362da4b8e3e066cdcc4
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841055"
---
# <a name="shellfolderviewocenumdone-event"></a><span data-ttu-id="3e3db-103">Шеллфолдервиевок. Енумдоне, событие</span><span class="sxs-lookup"><span data-stu-id="3e3db-103">ShellFolderViewOC.EnumDone event</span></span>

<span data-ttu-id="3e3db-104">Указывает, что объект [**шеллфолдервиев**](shellfolderview.md) завершил перечисление содержимого папки.</span><span class="sxs-lookup"><span data-stu-id="3e3db-104">Indicates that the [**ShellFolderView**](shellfolderview.md) object has finished enumerating the folder's contents.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e3db-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3e3db-105">Syntax</span></span>


```JScript
function EventHandler()
{
    // Code to handle the event.
}

// Set the event property to the handler.
ShellFolderViewOC.EnumDone = EventHandler;
```



## <a name="parameters"></a><span data-ttu-id="3e3db-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3e3db-106">Parameters</span></span>

<span data-ttu-id="3e3db-107">Этот обработчик событий не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3e3db-107">This event handler has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e3db-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="3e3db-108">Remarks</span></span>

<span data-ttu-id="3e3db-109">Объект [**шеллфолдервиев**](shellfolderview.md) должен перечислить содержимое папки, прежде чем она сможет ее отобразить.</span><span class="sxs-lookup"><span data-stu-id="3e3db-109">The [**ShellFolderView**](shellfolderview.md) object must enumerate the contents of a folder before it can display it.</span></span> <span data-ttu-id="3e3db-110">При наличии больших или расположенных в удаленной системе папок Этот процесс может занять несколько минут.</span><span class="sxs-lookup"><span data-stu-id="3e3db-110">With folders that are large or located on a remote system, this process can take as much as several minutes.</span></span> <span data-ttu-id="3e3db-111">В течение этого времени отображается анимированный рисунок фонарик, указывающий пользователю, что обработка выполняется по-разному.</span><span class="sxs-lookup"><span data-stu-id="3e3db-111">During this time, an animated flashlight graphic is displayed to indicate to the user that processing is under way.</span></span> <span data-ttu-id="3e3db-112">После перечисления будет вызвано событие **енумдоне** , и изображение фонарик заменяется содержимым папки.</span><span class="sxs-lookup"><span data-stu-id="3e3db-112">Once the enumeration is complete, the **EnumDone** event is fired and the flashlight graphic is replaced by the contents of the folder.</span></span>

<span data-ttu-id="3e3db-113">Укажите код обработки событий для этого события, как показано здесь.</span><span class="sxs-lookup"><span data-stu-id="3e3db-113">Provide event handling code for this event as shown here.</span></span>


```
 
Private Sub object_EnumDone()
    'Event handling code
End Sub
                
```



## <a name="requirements"></a><span data-ttu-id="3e3db-114">Requirements (Требования)</span><span class="sxs-lookup"><span data-stu-id="3e3db-114">Requirements</span></span>



| <span data-ttu-id="3e3db-115">Требование</span><span class="sxs-lookup"><span data-stu-id="3e3db-115">Requirement</span></span> | <span data-ttu-id="3e3db-116">Значение</span><span class="sxs-lookup"><span data-stu-id="3e3db-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e3db-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3e3db-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e3db-118">Windows 2000 Professional, только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3e3db-118">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3e3db-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3e3db-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e3db-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3e3db-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3e3db-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3e3db-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e3db-122"><dt>Шлдисп. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e3db-122"><dt>Shldisp.h</dt></span></span> </dl>                          |
| <span data-ttu-id="3e3db-123">IDL</span><span class="sxs-lookup"><span data-stu-id="3e3db-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3e3db-124"><dt>Шлдисп. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3e3db-124"><dt>Shldisp.idl</dt></span></span> </dl>                        |
| <span data-ttu-id="3e3db-125">DLL</span><span class="sxs-lookup"><span data-stu-id="3e3db-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3e3db-126"><dt>Shell32.dll (версия 5,0 или более поздняя)</dt></span><span class="sxs-lookup"><span data-stu-id="3e3db-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e3db-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3e3db-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e3db-128">**шеллфолдервиевок**</span><span class="sxs-lookup"><span data-stu-id="3e3db-128">**ShellFolderViewOC**</span></span>](shellfolderviewoc-object.md)
</dt> </dl>

 

 




