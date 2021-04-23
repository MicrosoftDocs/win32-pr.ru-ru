---
title: Изменения в модели режима IME
description: Модель режима IME изменена с "на пользователя" на "на поток"
ms.assetid: C9717AF2-7055-47CA-8F8F-BC0F483B2259
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 781c322949f17d4d3313b6a9b7b5eff9b1e83b06
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338836"
---
# <a name="ime-mode-model-changed-from-per-user-to-per-thread"></a><span data-ttu-id="a0c29-103">Модель режима IME изменена с "на пользователя" на "на поток"</span><span class="sxs-lookup"><span data-stu-id="a0c29-103">IME mode model changed from per-user to per-thread</span></span>

## <a name="platforms"></a><span data-ttu-id="a0c29-104">Платформы</span><span class="sxs-lookup"><span data-stu-id="a0c29-104">Platforms</span></span>

<dl> <span data-ttu-id="a0c29-105">Клиенты — Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="a0c29-105">Clients - Windows 8.1</span></span>  
<span data-ttu-id="a0c29-106">Серверы — Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="a0c29-106">Servers - Windows Server 2012 R2</span></span>  
</dl>

## <a name="description"></a><span data-ttu-id="a0c29-107">Описание</span><span class="sxs-lookup"><span data-stu-id="a0c29-107">Description</span></span>

<span data-ttu-id="a0c29-108">В Windows 8 режим преобразования IME и режим предложений IME основаны на контексте пользователя и изменяют режим приложения, затронутый всеми другими приложениями.</span><span class="sxs-lookup"><span data-stu-id="a0c29-108">In Windows 8, the IME Conversion Mode and IME Sentence Mode were based on the User context, and changing the mode of an application affected all other applications.</span></span> <span data-ttu-id="a0c29-109">Это поведение можно отключить с помощью параметра "Позвольте мне задать другой метод ввода для каждого окна приложения" в разделе "Дополнительные параметры" панели управления "язык".</span><span class="sxs-lookup"><span data-stu-id="a0c29-109">This behavior could be disabled by using the "Let me set a different input method for each app window" setting in the advanced settings section of the language control panel.</span></span>

<span data-ttu-id="a0c29-110">Чтобы улучшить совместимость, в Windows 8.1 режимы хранятся во входном контексте независимо от того, как установлен элемент управления "разрешить мне устанавливать различные методы ввода для каждого окна приложения".</span><span class="sxs-lookup"><span data-stu-id="a0c29-110">In order to improve compatibility, in Windows 8.1 the modes are stored in an Input context regardless of how the "Let me set a different input method for each app window" control is set.</span></span> <span data-ttu-id="a0c29-111">В Windows 8.1 параметр «позвольте мне задать другой метод ввода для каждого окна приложения» влияет только на выбор самого метода ввода.</span><span class="sxs-lookup"><span data-stu-id="a0c29-111">In Windows 8.1, the "Let me set a different input method for each app window" setting affects only the selection of the input method itself.</span></span>

<span data-ttu-id="a0c29-112">При запуске приложения в режиме IME задаются следующие значения по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="a0c29-112">At application start up, the IME mode is set to the following defaults:</span></span>



|          | <span data-ttu-id="a0c29-113">Панель программного ввода</span><span class="sxs-lookup"><span data-stu-id="a0c29-113">Software input panel</span></span> | <span data-ttu-id="a0c29-114">Аппаратная клавиатура</span><span class="sxs-lookup"><span data-stu-id="a0c29-114">Hardware keyboard</span></span> |
|----------|----------------------|-------------------|
| <span data-ttu-id="a0c29-115">KOR, JPN</span><span class="sxs-lookup"><span data-stu-id="a0c29-115">KOR, JPN</span></span> | <span data-ttu-id="a0c29-116">С</span><span class="sxs-lookup"><span data-stu-id="a0c29-116">On</span></span>                   | <span data-ttu-id="a0c29-117">Выкл.</span><span class="sxs-lookup"><span data-stu-id="a0c29-117">Off</span></span>               |
| <span data-ttu-id="a0c29-118">CHS, CHT</span><span class="sxs-lookup"><span data-stu-id="a0c29-118">CHS,CHT</span></span>  | <span data-ttu-id="a0c29-119">Включено</span><span class="sxs-lookup"><span data-stu-id="a0c29-119">On</span></span>                   | <span data-ttu-id="a0c29-120">Включено</span><span class="sxs-lookup"><span data-stu-id="a0c29-120">On</span></span>                |



 

## <a name="manifestations"></a><span data-ttu-id="a0c29-121">Проявлениями</span><span class="sxs-lookup"><span data-stu-id="a0c29-121">Manifestations</span></span>

<span data-ttu-id="a0c29-122">Когда пользователь изменяет режим IME в приложении, это изменение не влияет на другие приложения.</span><span class="sxs-lookup"><span data-stu-id="a0c29-122">When a user changes the IME mode on an application, the change doesn’t affect other applications.</span></span>

## <a name="resources"></a><span data-ttu-id="a0c29-123">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="a0c29-123">Resources</span></span>

-   [<span data-ttu-id="a0c29-124">Значения режима преобразования IME</span><span class="sxs-lookup"><span data-stu-id="a0c29-124">IME Conversion Mode Values</span></span>](../intl/ime-conversion-mode-values.md)
-   [<span data-ttu-id="a0c29-125">Значения режима предложений IME</span><span class="sxs-lookup"><span data-stu-id="a0c29-125">IME Sentence Mode Values</span></span>](../intl/ime-sentence-mode-values.md)

 

 