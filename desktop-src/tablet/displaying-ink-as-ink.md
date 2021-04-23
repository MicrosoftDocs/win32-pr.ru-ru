---
description: Поведением элемента управления InkEdit по умолчанию является распознавание и преобразование рукописного ввода в текст по истечении короткого времени ожидания.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Отображение рукописного ввода в виде рукописного текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693472"
---
# <a name="displaying-ink-as-ink"></a><span data-ttu-id="fa985-103">Отображение рукописного ввода в виде рукописного текста</span><span class="sxs-lookup"><span data-stu-id="fa985-103">Displaying Ink as Ink</span></span>

<span data-ttu-id="fa985-104">Поведением элемента управления [InkEdit](inkedit-control-reference.md) по умолчанию является распознавание и преобразование рукописного ввода в текст по истечении короткого времени ожидания.</span><span class="sxs-lookup"><span data-stu-id="fa985-104">The default behavior for the [InkEdit](inkedit-control-reference.md) control is to recognize and convert ink into text after a brief timeout has expired.</span></span> <span data-ttu-id="fa985-105">Поскольку элемент управления является суперклассом [RichEdit](../controls/rich-edit-controls.md), можно также встроить и отобразить рукописный ввод в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="fa985-105">Because the control is a superclass of [RichEdit](../controls/rich-edit-controls.md), it is also possible to embed and display ink within the control.</span></span> <span data-ttu-id="fa985-106">Каждое слово вставляется в элемент управления как объект [**инкдисп**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="fa985-106">Each word is inserted into the control as an [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="fa985-107">Объект **инкдисп** содержит рукописный ввод и его варианты распознавания.</span><span class="sxs-lookup"><span data-stu-id="fa985-107">The **InkDisp** object contains the ink and its recognition alternates.</span></span>

<span data-ttu-id="fa985-108">При вставке рукописный ввод масштабируется до текущего размера шрифта и других внешних свойств, таких как курсив или полужирный шрифт.</span><span class="sxs-lookup"><span data-stu-id="fa985-108">When inserted, the ink is scaled to the current font size and other ambient properties, such as italics or bold, are applied.</span></span> <span data-ttu-id="fa985-109">Если пользователь выбирает изменение текста объекта [**инкдисп**](inkdisp-class.md) , он должен сначала преобразовать рукописный ввод в текст.</span><span class="sxs-lookup"><span data-stu-id="fa985-109">If the user chooses to edit the text of an [**InkDisp**](inkdisp-class.md) object, he or she must first convert the ink to text.</span></span>

> [!Note]  
> <span data-ttu-id="fa985-110">Во время преобразования все рукописные данные и распознавание альтернативных данных теряются.</span><span class="sxs-lookup"><span data-stu-id="fa985-110">All ink and recognition alternate data is lost during the conversion.</span></span>

 

<span data-ttu-id="fa985-111">Эта функция доступна только на компьютерах под управлением Microsoft Windows XP Tablet PC Edition, Windows Vista или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="fa985-111">This feature is available only on computers that run Microsoft Windows XP Tablet PC Edition, Windows Vista, or later.</span></span>

 

 
