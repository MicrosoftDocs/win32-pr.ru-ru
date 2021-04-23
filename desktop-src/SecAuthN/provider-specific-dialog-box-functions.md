---
description: Функции диалогового окна, зависящие от поставщика, позволяют поставщику отображать и обменять информацию, относящуюся к сети, путем изменения системных диалоговых окон или отображения пользовательских диалоговых окон.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Функции диалогового окна Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647593"
---
# <a name="provider-specific-dialog-box-functions"></a><span data-ttu-id="6d81e-103">Функции диалогового окна Provider-Specific</span><span class="sxs-lookup"><span data-stu-id="6d81e-103">Provider-Specific Dialog Box Functions</span></span>

<span data-ttu-id="6d81e-104">Функции диалогового окна, зависящие от поставщика, позволяют поставщику отображать и обменять информацию, относящуюся к сети, путем изменения системных диалоговых окон или отображения пользовательских диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="6d81e-104">Provider-specific dialog box functions enable a provider to display and handle network-specific information by altering system dialog boxes or displaying custom dialog boxes.</span></span>

<span data-ttu-id="6d81e-105">Следующие функции диалогового окна добавляют кнопки в диалоговое окно **Свойства** диспетчера файлов.</span><span class="sxs-lookup"><span data-stu-id="6d81e-105">The following dialog box functions add buttons to the File Manager **Properties** dialog box.</span></span> <span data-ttu-id="6d81e-106">Затем поставщик может управлять событиями этих кнопок для выполнения задач, связанных с сетью.</span><span class="sxs-lookup"><span data-stu-id="6d81e-106">The provider can then handle the events of those buttons to perform network-specific tasks.</span></span> <span data-ttu-id="6d81e-107">Обратите внимание, что количество кнопок, которые можно добавить, ограничено.</span><span class="sxs-lookup"><span data-stu-id="6d81e-107">Note that there is a limit to the number of buttons that can be added.</span></span> <span data-ttu-id="6d81e-108">По этой причине поставщики должны использовать эту возможность экономно.</span><span class="sxs-lookup"><span data-stu-id="6d81e-108">Because of this, providers should use this capability sparingly.</span></span> <span data-ttu-id="6d81e-109">Кроме того, поставщик может не иметь возможности добавить кнопку, так как доступное место уже используется другими поставщиками.</span><span class="sxs-lookup"><span data-stu-id="6d81e-109">Also, a provider may find itself unable to add a button because the available space has been used already by other providers.</span></span> <span data-ttu-id="6d81e-110">Поставщик сети должен справиться с этой ситуацией.</span><span class="sxs-lookup"><span data-stu-id="6d81e-110">A network provider should handle this situation.</span></span>



| <span data-ttu-id="6d81e-111">Функция</span><span class="sxs-lookup"><span data-stu-id="6d81e-111">Function</span></span>                                           | <span data-ttu-id="6d81e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="6d81e-112">Description</span></span>                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d81e-113">**нпжетпропертитекст**</span><span class="sxs-lookup"><span data-stu-id="6d81e-113">**NPGetPropertyText**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | <span data-ttu-id="6d81e-114">Определяет имена кнопок, добавляемых в диалоговое окно Свойства для определенного ресурса.</span><span class="sxs-lookup"><span data-stu-id="6d81e-114">Determines the names of buttons added to a property dialog box for a specific resource.</span></span><br/>                                      |
| [<span data-ttu-id="6d81e-115">**нппропертидиалог**</span><span class="sxs-lookup"><span data-stu-id="6d81e-115">**NPPropertyDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | <span data-ttu-id="6d81e-116">Вызывается, когда пользователь нажимает кнопку, добавленную с помощью функции [**нпжетпропертитекст**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .</span><span class="sxs-lookup"><span data-stu-id="6d81e-116">Called when a user clicks a button added by using the [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) function.</span></span><br/>               |
| [<span data-ttu-id="6d81e-117">**нпсеарчдиалог**</span><span class="sxs-lookup"><span data-stu-id="6d81e-117">**NPSearchDialog**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | <span data-ttu-id="6d81e-118">Позволяет поставщикам сети реализовывать собственные функции поиска, помимо указанных в диалоговом окне **соединения** .</span><span class="sxs-lookup"><span data-stu-id="6d81e-118">Enables network providers to implement their own search functionality beyond that provided in the **Connection** dialog box.</span></span><br/> |
| [<span data-ttu-id="6d81e-119">**нпформатнетворкнаме**</span><span class="sxs-lookup"><span data-stu-id="6d81e-119">**NPFormatNetworkName**</span></span>](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | <span data-ttu-id="6d81e-120">Позволяет поставщикам сети форматировать или иным образом изменять сетевые имена, прежде чем они будут представлены пользователю.</span><span class="sxs-lookup"><span data-stu-id="6d81e-120">Enables network providers to format or otherwise modify network names before they are presented to the user.</span></span><br/>                 |



 

 

 




