---
description: В этом разделе описываются интерфейсы IMM.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Интерфейсы диспетчера методов ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683520"
---
# <a name="input-method-manager-interfaces"></a><span data-ttu-id="62660-103">Интерфейсы диспетчера методов ввода</span><span class="sxs-lookup"><span data-stu-id="62660-103">Input Method Manager Interfaces</span></span>

<span data-ttu-id="62660-104">В этом разделе описываются интерфейсы IMM.</span><span class="sxs-lookup"><span data-stu-id="62660-104">This section describes the IMM interfaces.</span></span>



| <span data-ttu-id="62660-105">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="62660-105">Interface</span></span>                                                            | <span data-ttu-id="62660-106">Описание</span><span class="sxs-lookup"><span data-stu-id="62660-106">Description</span></span>                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="62660-107">**ифекоммон**</span><span class="sxs-lookup"><span data-stu-id="62660-107">**IFECommon**</span></span>](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | <span data-ttu-id="62660-108">Предоставляет службы, связанные с IME, которые являются общими для разных языков.</span><span class="sxs-lookup"><span data-stu-id="62660-108">Provides IME-related services that are common for different languages.</span></span>                                                                         |
| [<span data-ttu-id="62660-109">**ифедиктионари**</span><span class="sxs-lookup"><span data-stu-id="62660-109">**IFEDictionary**</span></span>](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | <span data-ttu-id="62660-110">Разрешает клиентам доступ к пользовательскому словарю Microsoft IME.</span><span class="sxs-lookup"><span data-stu-id="62660-110">Allows clients to access a Microsoft IME user dictionary.</span></span>                                                                                      |
| [<span data-ttu-id="62660-111">**ифелангуаже**</span><span class="sxs-lookup"><span data-stu-id="62660-111">**IFELanguage**</span></span>](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | <span data-ttu-id="62660-112">Предоставляет службы языковой обработки с помощью редактора IME (Майкрософт).</span><span class="sxs-lookup"><span data-stu-id="62660-112">Provides language processing services using the Microsoft IME.</span></span>                                                                                 |
| [<span data-ttu-id="62660-113">**иимепад**</span><span class="sxs-lookup"><span data-stu-id="62660-113">**IImePad**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | <span data-ttu-id="62660-114">Вставляет текст в приложения из Имепадапплетс, которые реализуют интерфейс [**иимепадапплет**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="62660-114">Inserts text into apps from IMEPadApplets that implement the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span>                                 |
| [<span data-ttu-id="62660-115">**иимепадапплет**</span><span class="sxs-lookup"><span data-stu-id="62660-115">**IImePadApplet**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | <span data-ttu-id="62660-116">Вводит строки в приложения через интерфейс [**иимепад**](/windows/desktop/api/Imepad/nn-imepad-iimepad) .</span><span class="sxs-lookup"><span data-stu-id="62660-116">Inputs strings into apps through the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface.</span></span>                                                                     |
| [<span data-ttu-id="62660-117">**иимеплугиндиктдиктионарилист**</span><span class="sxs-lookup"><span data-stu-id="62660-117">**IImePlugInDictDictionaryList**</span></span>](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | <span data-ttu-id="62660-118">Предоставляет доступ к списку словарей подключаемых модулей IME.</span><span class="sxs-lookup"><span data-stu-id="62660-118">Provides access to the list of IME plug-in dictionaries.</span></span>                                                                                       |
| [<span data-ttu-id="62660-119">**иимеспеЦифяпплетс**</span><span class="sxs-lookup"><span data-stu-id="62660-119">**IImeSpecifyApplets**</span></span>](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | <span data-ttu-id="62660-120">Указывает методы, вызываемые из объекта интерфейса [**иимепад**](/windows/desktop/api/Imepad/nn-imepad-iimepad) для эмуляции интерфейса [**иимепадапплет**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) .</span><span class="sxs-lookup"><span data-stu-id="62660-120">Specifies methods called from the [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) interface object to emulate the [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) interface.</span></span> |



 

 

 



