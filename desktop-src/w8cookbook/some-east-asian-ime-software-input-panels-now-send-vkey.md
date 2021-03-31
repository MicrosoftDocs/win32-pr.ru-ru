---
title: Некоторые панели ввода программного обеспечения IME для восточноазиатских языков теперь отправляют ключ
description: Некоторые панели ввода программного обеспечения IME для восточноазиатских языков теперь отправляют ключ
ms.assetid: 5E3BE112-D962-4C11-B31E-229584191FAE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c444091e4498582cccc4378dfa2f17216cbf810
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103889248"
---
# <a name="some-east-asian-ime-software-input-panels-now-send-vkey"></a><span data-ttu-id="620f8-103">Некоторые панели ввода программного обеспечения IME для восточноазиатских языков теперь отправляют ключ</span><span class="sxs-lookup"><span data-stu-id="620f8-103">Some East Asian IME software input panels now send vKey</span></span>

## <a name="platforms"></a><span data-ttu-id="620f8-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="620f8-104">Platforms</span></span>

<dl> <span data-ttu-id="620f8-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="620f8-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="620f8-106">Серверы — Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="620f8-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="620f8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="620f8-107">Description</span></span>

<span data-ttu-id="620f8-108">В Windows 8, если выбран один из восточно-азиатских языков IME, при нажатии клавиши на панели ввода программного обеспечения не была отправлена Вкэйс.</span><span class="sxs-lookup"><span data-stu-id="620f8-108">In Windows 8, if one of the East Asian IMEs is selected, pressing a software input panel key did not send vKeys.</span></span>

<span data-ttu-id="620f8-109">В Windows 8.1 отправляются Вкэйс для следующих конфигураций:</span><span class="sxs-lookup"><span data-stu-id="620f8-109">In Windows 8.1, vKeys are sent for the following configurations:</span></span>



| <span data-ttu-id="620f8-110">Язык</span><span class="sxs-lookup"><span data-stu-id="620f8-110">Language</span></span>            | <span data-ttu-id="620f8-111">IME</span><span class="sxs-lookup"><span data-stu-id="620f8-111">IME</span></span>                                 | <span data-ttu-id="620f8-112">Магазин Windows</span><span class="sxs-lookup"><span data-stu-id="620f8-112">Windows Store</span></span> | <span data-ttu-id="620f8-113">Персональный компьютер</span><span class="sxs-lookup"><span data-stu-id="620f8-113">Desktop</span></span> |
|---------------------|-------------------------------------|---------------|---------|
| <span data-ttu-id="620f8-114">Китайский (упрощенный)</span><span class="sxs-lookup"><span data-stu-id="620f8-114">Simplified Chinese</span></span>  | <span data-ttu-id="620f8-115">Пиньинь Майкрософт, Microsoft Wubi</span><span class="sxs-lookup"><span data-stu-id="620f8-115">Microsoft Pinyin, Microsoft Wubi</span></span>    | <span data-ttu-id="620f8-116">Да</span><span class="sxs-lookup"><span data-stu-id="620f8-116">Yes</span></span>           | <span data-ttu-id="620f8-117">Да</span><span class="sxs-lookup"><span data-stu-id="620f8-117">Yes</span></span>     |
| <span data-ttu-id="620f8-118">Китайский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="620f8-118">Traditional Chinese</span></span> | <span data-ttu-id="620f8-119">Microsoft Чанглие, Microsoft Quick</span><span class="sxs-lookup"><span data-stu-id="620f8-119">Microsoft Changlie, Microsoft Quick</span></span> | <span data-ttu-id="620f8-120">Да</span><span class="sxs-lookup"><span data-stu-id="620f8-120">Yes</span></span>           | <span data-ttu-id="620f8-121">Да</span><span class="sxs-lookup"><span data-stu-id="620f8-121">Yes</span></span>     |
| <span data-ttu-id="620f8-122">Китайский (традиционный)</span><span class="sxs-lookup"><span data-stu-id="620f8-122">Traditional Chinese</span></span> | <span data-ttu-id="620f8-123">Бопомофо (Майкрософт)</span><span class="sxs-lookup"><span data-stu-id="620f8-123">Microsoft Bopomofo</span></span>                  | <span data-ttu-id="620f8-124">Нет</span><span class="sxs-lookup"><span data-stu-id="620f8-124">No</span></span>            | <span data-ttu-id="620f8-125">Нет</span><span class="sxs-lookup"><span data-stu-id="620f8-125">No</span></span>      |
| <span data-ttu-id="620f8-126">Корейский</span><span class="sxs-lookup"><span data-stu-id="620f8-126">Korean</span></span>              | <span data-ttu-id="620f8-127">"Microsoft IME"</span><span class="sxs-lookup"><span data-stu-id="620f8-127">Microsoft IME</span></span>                       | <span data-ttu-id="620f8-128">Да</span><span class="sxs-lookup"><span data-stu-id="620f8-128">Yes</span></span>           | <span data-ttu-id="620f8-129">Нет</span><span class="sxs-lookup"><span data-stu-id="620f8-129">No</span></span>      |
| <span data-ttu-id="620f8-130">Японский</span><span class="sxs-lookup"><span data-stu-id="620f8-130">Japanese</span></span>            | <span data-ttu-id="620f8-131">"Microsoft IME"</span><span class="sxs-lookup"><span data-stu-id="620f8-131">Microsoft IME</span></span>                       | <span data-ttu-id="620f8-132">Нет</span><span class="sxs-lookup"><span data-stu-id="620f8-132">No</span></span>            | <span data-ttu-id="620f8-133">Нет</span><span class="sxs-lookup"><span data-stu-id="620f8-133">No</span></span>      |



 

## <a name="manifestations"></a><span data-ttu-id="620f8-134">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="620f8-134">Manifestations</span></span>

<span data-ttu-id="620f8-135">Если пользователь выбирает IME, который не отправляет Вкэйс, функции, активируемые с помощью триггера, не работают.</span><span class="sxs-lookup"><span data-stu-id="620f8-135">If the user chooses an IME that does not send vKeys, vKey-triggered functions do not work.</span></span>

## <a name="solution"></a><span data-ttu-id="620f8-136">Решение</span><span class="sxs-lookup"><span data-stu-id="620f8-136">Solution</span></span>

<span data-ttu-id="620f8-137">Приложения, которые не используют одну из перечисленных выше конфигураций IME, должны быть спроектированы таким образом, чтобы пользователи могли выполнять нужную задачу без использования функций, требующих Вкэйс.</span><span class="sxs-lookup"><span data-stu-id="620f8-137">Applications that do not use one of the above IME configurations must be designed so that users can complete the desired task without using functions that require vKeys.</span></span>

<span data-ttu-id="620f8-138">Если пользователь выбирает IME, который отправляет Вкэйс, но приложение было спроектировано без этого ожидания, приложение должно быть изменено, чтобы определить, какая версия Windows работает, и ответить соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="620f8-138">If the user chooses an IME that does send vKeys, but the application was designed without that expectation, the application must be changed to recognize which version of Windows is running and respond accordingly.</span></span>

 

 




