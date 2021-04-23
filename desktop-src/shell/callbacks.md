---
description: В этом разделе описываются функции обратного вызова оболочки Windows.
title: Функции обратного вызова оболочки
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 617a73d9-e3e6-4def-a5b2-557faa7b03c0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f6ae93437caa740c8c1349690b7e1452a032491
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423718"
---
# <a name="shell-callback-functions"></a><span data-ttu-id="7b795-103">Функции обратного вызова оболочки</span><span class="sxs-lookup"><span data-stu-id="7b795-103">Shell Callback Functions</span></span>

<span data-ttu-id="7b795-104">В этом разделе описываются функции обратного вызова оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="7b795-104">This section describes the Windows Shell callback functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="7b795-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="7b795-105">In this section</span></span>



| <span data-ttu-id="7b795-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="7b795-106">Topic</span></span>                                                                     | <span data-ttu-id="7b795-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7b795-107">Description</span></span>                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b795-108">[**бффкаллбакк**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7b795-108">[**BFFCALLBACK**](/previous-versions/windows/desktop/legacy/bb762598(v=vs.85))</span></span><br/>                      | <span data-ttu-id="7b795-109">Задает определяемую приложением функцию обратного вызова, используемую для отправки сообщений в, и обработки сообщений в диалоговом окне **обзора** , которое отображается в ответ на вызов [**шбровсефорфолдер**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span><span class="sxs-lookup"><span data-stu-id="7b795-109">Specifies an application-defined callback function used to send messages to, and process messages from, a **Browse** dialog box displayed in response to a call to [**SHBrowseForFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbrowseforfoldera).</span></span><br/> |
| [<span data-ttu-id="7b795-110">*фмекстенсионпрок*</span><span class="sxs-lookup"><span data-stu-id="7b795-110">*FMExtensionProc*</span></span>](fmextensionproc.md)<br/>                       | <span data-ttu-id="7b795-111">Указывает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов для взаимодействия с расширением диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="7b795-111">Specifies an application-defined callback function called by File Manager to communicate with a File Manager extension.</span></span><br/>                                                                                            |
| [<span data-ttu-id="7b795-112">*мрукмппрок*</span><span class="sxs-lookup"><span data-stu-id="7b795-112">*MRUCMPPROC*</span></span>](mrucmpproc.md)<br/>                                 | <span data-ttu-id="7b795-113">Используется для определения наличия элемента в списке последних использованных элементов.</span><span class="sxs-lookup"><span data-stu-id="7b795-113">Used to determine whether an item is present in a most recently used (MRU) list.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="7b795-114">**\_подпрограммы изменения паппстате \_**</span><span class="sxs-lookup"><span data-stu-id="7b795-114">**PAPPSTATE\_CHANGE\_ROUTINE**</span></span>](/windows/desktop/api/appnotify/nc-appnotify-pappstate_change_routine)<br/> | <span data-ttu-id="7b795-115">Указывает определяемую приложением функцию обратного вызова, которая уведомляет приложение о том, что приложение переходит в приостановленное состояние или выходит из него.</span><span class="sxs-lookup"><span data-stu-id="7b795-115">Specifies an app-defined callback function that notifies the app when the app is entering or leaving a suspended state.</span></span><br/>                                                                                            |
| [<span data-ttu-id="7b795-116">**субкласспрок**</span><span class="sxs-lookup"><span data-stu-id="7b795-116">**SUBCLASSPROC**</span></span>](/windows/win32/api/commctrl/nc-commctrl-subclassproc)<br/>                  | <span data-ttu-id="7b795-117">Определяет прототип функции обратного вызова, используемой [**ремовевиндовсубкласс**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) и [**сетвиндовсубкласс**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span><span class="sxs-lookup"><span data-stu-id="7b795-117">Defines the prototype for the callback function used by [**RemoveWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-removewindowsubclass) and [**SetWindowSubclass**](/windows/desktop/api/Commctrl/nf-commctrl-setwindowsubclass).</span></span><br/>                                                   |
| [<span data-ttu-id="7b795-118">**\_процедура отмены удаления \_ FM**</span><span class="sxs-lookup"><span data-stu-id="7b795-118">**FM\_UNDELETE\_PROC**</span></span>](undeletefile.md)<br/>                     | <span data-ttu-id="7b795-119">Задает определяемую приложением функцию обратного вызова, вызываемую диспетчером файлов, когда пользователь выбирает команду " **Отменить удаление** " в меню " **файл** ".</span><span class="sxs-lookup"><span data-stu-id="7b795-119">Specifies an application-defined callback function called by File Manager when the user chooses the **Undelete** command from the **File** menu.</span></span><br/>                                                                   |



 

 

 
