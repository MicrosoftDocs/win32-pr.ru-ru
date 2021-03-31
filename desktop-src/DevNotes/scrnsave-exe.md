---
description: '\\Рабочий стол панели управления HKCU \\ .'
ms.assetid: e18ea3c8-ddac-4214-83be-106c28c3c327
title: SCRNSAVE.EXE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77d6a5d50b002299fe38508b387926b0eed11141
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423426"
---
# <a name="scrnsaveexe"></a><span data-ttu-id="c2a2a-103">SCRNSAVE.EXE</span><span class="sxs-lookup"><span data-stu-id="c2a2a-103">SCRNSAVE.EXE</span></span>

<span data-ttu-id="c2a2a-104">**\\Рабочий стол панели управления HKCU \\**</span><span class="sxs-lookup"><span data-stu-id="c2a2a-104">**HKCU\\Control Panel\\Desktop**</span></span>



| <span data-ttu-id="c2a2a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c2a2a-105">Data type</span></span> | <span data-ttu-id="c2a2a-106">Диапазон</span><span class="sxs-lookup"><span data-stu-id="c2a2a-106">Range</span></span>       | <span data-ttu-id="c2a2a-107">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="c2a2a-107">Default value</span></span> |
|-----------|-------------|---------------|
| <span data-ttu-id="c2a2a-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="c2a2a-108">REG\_SZ</span></span>   | <span data-ttu-id="c2a2a-109">*Имя файла*</span><span class="sxs-lookup"><span data-stu-id="c2a2a-109">*File name*</span></span> | <span data-ttu-id="c2a2a-110">(нет)</span><span class="sxs-lookup"><span data-stu-id="c2a2a-110">(None)</span></span>        |



 

## <a name="description"></a><span data-ttu-id="c2a2a-111">Описание</span><span class="sxs-lookup"><span data-stu-id="c2a2a-111">Description</span></span>

<span data-ttu-id="c2a2a-112">Указывает имя исполняемого файла экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-112">Specifies the name of the screen saver executable file.</span></span>

## <a name="change-method"></a><span data-ttu-id="c2a2a-113">Изменение метода</span><span class="sxs-lookup"><span data-stu-id="c2a2a-113">Change Method</span></span>

<span data-ttu-id="c2a2a-114">Чтобы изменить значение этой записи, на панели управления дважды щелкните элемент " **экран**", перейдите на **вкладку "Заставка"** и выберите заставку из списка **экранных заставок** .</span><span class="sxs-lookup"><span data-stu-id="c2a2a-114">To change the value of this entry, in Control Panel double-click **Display**, click the **Screen Saver** tab, and then select a screen saver from the **Screen saver** list.</span></span>

<span data-ttu-id="c2a2a-115">Эту запись также можно изменить с помощью функции интерфейса прикладного программирования (API) **инсталлскринсавер**, которая экспортируется Desk.cpl.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-115">You can also change this entry with the application programming interface (API) function **InstallScreenSaver**, which is exported by Desk.cpl.</span></span> <span data-ttu-id="c2a2a-116">Доступ к этой функции можно получить с помощью командной строки **rundll32.exe desk.cpl, инсталлскринсавер** *File*, где *File* — это имя исполняемого файла экранной заставки.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-116">You can access this function with the command line **rundll32.exe desk.cpl,InstallScreenSaver** *file*, where *file* is the name of a screen saver executable file.</span></span>

## <a name="activation-method"></a><span data-ttu-id="c2a2a-117">Метод активации</span><span class="sxs-lookup"><span data-stu-id="c2a2a-117">Activation Method</span></span>

<span data-ttu-id="c2a2a-118">Изменения, внесенные в эту запись, вступают в силу в следующий раз, когда система запускает экранную заставку.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-118">Changes made to this entry become effective the next time the system starts a screen saver.</span></span> <span data-ttu-id="c2a2a-119">Изменения, внесенные в эту запись во время работы экранной заставки, не влияют на работу с экранной заставкой.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-119">Changes made to this entry while a screen saver is running have no effect on the running screen saver.</span></span>

## <a name="notes"></a><span data-ttu-id="c2a2a-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c2a2a-120">Notes</span></span>

-   <span data-ttu-id="c2a2a-121">Операционные системы Windows добавляют эту **запись в реестр при использовании экрана** в панели управления для выбора заставки.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-121">Windows operating systems add this entry to the registry when you use **Display** in Control Panel to select a screen saver.</span></span> <span data-ttu-id="c2a2a-122">Если отключить все экранные заставки, выбрав **(нет)** в списке экранная заставка, операционная система удаляет эту запись из реестра и вызывает функцию [**системпараметерсинфо**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) с параметром *уиактион* , равным SPI \_ сетскринсавеактиве, а *уипарам* равно **false**.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-122">If you disable all screen savers by choosing **(None)** from the screen saver list, then the operating system deletes this entry from the registry and calls the [**SystemParametersInfo**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) function with *uiAction* equal to SPI\_SETSCREENSAVEACTIVE and *uiParam* equal to **FALSE**.</span></span>
-   <span data-ttu-id="c2a2a-123">Эта запись может быть заменена параметром групповая политика в системах, поддерживающих групповая политика.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-123">This entry can be superseded by a Group Policy setting on systems that support Group Policy.</span></span> <span data-ttu-id="c2a2a-124">Хотя параметр групповая политика **имя исполняемого файла заставки** включен, система пропускает эту запись.</span><span class="sxs-lookup"><span data-stu-id="c2a2a-124">While the **Screen saver executable name** Group Policy setting is enabled, the system ignores this entry.</span></span> <span data-ttu-id="c2a2a-125">Конфигурация этого параметра политики хранится в записи **SCRNSAVE.EXE** , которая находится в подразделе " **политики** ".</span><span class="sxs-lookup"><span data-stu-id="c2a2a-125">The configuration of this policy setting is stored in the **SCRNSAVE.EXE** entry, which is in the **Policies** subkey.</span></span>

 

 
