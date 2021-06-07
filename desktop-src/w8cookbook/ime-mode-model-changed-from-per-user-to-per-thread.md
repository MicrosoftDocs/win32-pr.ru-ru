---
title: Изменения в модели режима IME
description: Модель режима IME изменена с "на пользователя" на "на поток"
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30404b1a386c4346e7d8900481d8c5198972cdbe
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111443251"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="359ec-103">Модель режима IME изменена с "на пользователя" на "на поток"</span><span class="sxs-lookup"><span data-stu-id="359ec-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="359ec-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="359ec-104">Platforms</span></span>

<dl> <span data-ttu-id="359ec-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="359ec-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="359ec-106">Серверы — Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="359ec-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="359ec-107">Описание</span><span class="sxs-lookup"><span data-stu-id="359ec-107">Description</span></span>

<span data-ttu-id="359ec-108">В Windows 8 режим преобразования IME и режим предложений IME основаны на контексте пользователя и изменяют режим приложения, затронутый всеми другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="359ec-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="359ec-109">Это поведение можно отключить с помощью параметра "Позвольте мне задать другой метод ввода для каждого окна приложения" в разделе "Дополнительные параметры" панели управления "язык".</span><span class="sxs-lookup"><span data-stu-id="359ec-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="359ec-110">Чтобы улучшить совместимость, в Windows 8.1 режимы хранятся во входном контексте независимо от того, как установлен элемент управления "разрешить мне устанавливать различные методы ввода для каждого окна приложения".</span><span class="sxs-lookup"><span data-stu-id="359ec-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="359ec-111">В Windows 8.1 параметр «позвольте мне задать другой метод ввода для каждого окна приложения» влияет только на выбор самого метода ввода.</span><span class="sxs-lookup"><span data-stu-id="359ec-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="359ec-112">При запуске приложения в режиме IME задаются следующие значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="359ec-112">At application start up, the IME mode is set to the following defaults:</span></span>



| &nbsp;   | <span data-ttu-id="359ec-113">Панель программного ввода</span><span class="sxs-lookup"><span data-stu-id="359ec-113">Software input panel</span></span> | <span data-ttu-id="359ec-114">Аппаратная клавиатура</span><span class="sxs-lookup"><span data-stu-id="359ec-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="359ec-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="359ec-115">KOR, JPN</span></span> | <span data-ttu-id="359ec-116">С</span><span class="sxs-lookup"><span data-stu-id="359ec-116">On</span></span>                   | <span data-ttu-id="359ec-117">Выкл.</span><span class="sxs-lookup"><span data-stu-id="359ec-117">Off</span></span>               |
| <span data-ttu-id="359ec-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="359ec-118">CHS,CHT</span></span>  | <span data-ttu-id="359ec-119">Включено</span><span class="sxs-lookup"><span data-stu-id="359ec-119">On</span></span>                   | <span data-ttu-id="359ec-120">Включено</span><span class="sxs-lookup"><span data-stu-id="359ec-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="359ec-121">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="359ec-121">Manifestations</span></span>

<span data-ttu-id="359ec-122">Когда пользователь изменяет режим IME в приложении, это изменение не влияет на другие приложения.</span><span class="sxs-lookup"><span data-stu-id="359ec-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="359ec-123">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="359ec-123">Resources</span></span>

-   [<span data-ttu-id="359ec-124">Значения режима преобразования IME</span><span class="sxs-lookup"><span data-stu-id="359ec-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="359ec-125">Значения режима предложений IME</span><span class="sxs-lookup"><span data-stu-id="359ec-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 