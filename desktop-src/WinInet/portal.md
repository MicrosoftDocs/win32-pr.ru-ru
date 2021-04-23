---
title: Windows Internet
description: Прикладной программный интерфейс (API) Microsoft Windows Internet (WinINet) позволяет приложениям получать доступ к стандартным протоколам Интернета, таким как FTP и HTTP. Чтобы упростить использование, WinINet абстрагирует эти протоколы в интерфейсе высокого уровня.
ms.assetid: 9d1856ac-f281-4582-bb70-83a8ec674914
keywords:
- Windows Internet WinINet
- WinINet WinINet, портал
- Windows Internet WinINet, начальная страница
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6b5b76fefea900d3f187deb89929d3a09fe3c78
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104488088"
---
# <a name="windows-internet"></a><span data-ttu-id="b4a89-107">Windows Internet</span><span class="sxs-lookup"><span data-stu-id="b4a89-107">Windows Internet</span></span>

## <a name="purpose"></a><span data-ttu-id="b4a89-108">Назначение</span><span class="sxs-lookup"><span data-stu-id="b4a89-108">Purpose</span></span>

<span data-ttu-id="b4a89-109">Прикладной программный интерфейс (API) Microsoft Windows Internet (WinINet) позволяет приложениям получать доступ к стандартным протоколам Интернета, таким как FTP и HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4a89-109">The Microsoft Windows Internet (WinINet) application programming interface (API) enables applications to access standard Internet protocols, such as FTP and HTTP.</span></span> <span data-ttu-id="b4a89-110">Чтобы упростить использование, WinINet абстрагирует эти протоколы в интерфейсе высокого уровня.</span><span class="sxs-lookup"><span data-stu-id="b4a89-110">For ease of use, WinINet abstracts these protocols into a high-level interface.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="b4a89-111">Где применимо</span><span class="sxs-lookup"><span data-stu-id="b4a89-111">Where applicable</span></span>

<span data-ttu-id="b4a89-112">WinINet не поддерживает реализации серверов.</span><span class="sxs-lookup"><span data-stu-id="b4a89-112">WinINet does not support server implementations.</span></span> <span data-ttu-id="b4a89-113">Кроме того, его не следует использовать из службы.</span><span class="sxs-lookup"><span data-stu-id="b4a89-113">In addition, it should not be used from a service.</span></span> <span data-ttu-id="b4a89-114">Для серверных реализаций или служб используйте [службы Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="b4a89-114">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="b4a89-115">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="b4a89-115">Developer audience</span></span>

<span data-ttu-id="b4a89-116">WinINet предназначен для использования программистами C/C++.</span><span class="sxs-lookup"><span data-stu-id="b4a89-116">WinINet is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="b4a89-117">Для этого требуется базовое понимание протоколов FTP и HTTP.</span><span class="sxs-lookup"><span data-stu-id="b4a89-117">It requires a basic understanding of the FTP and HTTP protocols.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="b4a89-118">Требования к среде выполнения</span><span class="sxs-lookup"><span data-stu-id="b4a89-118">Run-time requirements</span></span>

<span data-ttu-id="b4a89-119">Для приложений, использующих API WinINet, требуется Windows NT 4,0 или более поздняя версия или Windows Me/98/95.</span><span class="sxs-lookup"><span data-stu-id="b4a89-119">Applications that use the WinINet API require Windows NT 4.0 or later, or Windows Me/98/95.</span></span> <span data-ttu-id="b4a89-120">Дополнительные сведения о том, какие операционные системы или компоненты необходимы для использования определенного программного элемента, см. в разделе "требования" документации.</span><span class="sxs-lookup"><span data-stu-id="b4a89-120">For more information about which operating systems or components are required to use a particular programming element, see the Requirements section of the documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="b4a89-121">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="b4a89-121">In this section</span></span>



| <span data-ttu-id="b4a89-122">Раздел</span><span class="sxs-lookup"><span data-stu-id="b4a89-122">Topic</span></span>                                                          | <span data-ttu-id="b4a89-123">Описание</span><span class="sxs-lookup"><span data-stu-id="b4a89-123">Description</span></span>                                                      |
|----------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="b4a89-124">О Windows Internet</span><span class="sxs-lookup"><span data-stu-id="b4a89-124">About Windows Internet</span></span>](about-wininet.md)<br/>         | <span data-ttu-id="b4a89-125">Общие сведения об API Windows в Интернете.</span><span class="sxs-lookup"><span data-stu-id="b4a89-125">General information about the Windows Internet API.</span></span><br/>   |
| [<span data-ttu-id="b4a89-126">Использование Windows Internet</span><span class="sxs-lookup"><span data-stu-id="b4a89-126">Using Windows Internet</span></span>](using-wininet.md)<br/>         | <span data-ttu-id="b4a89-127">Инструкции по программированию для Windows Internet API.</span><span class="sxs-lookup"><span data-stu-id="b4a89-127">Programming guide for the Windows Internet API.</span></span><br/>       |
| [<span data-ttu-id="b4a89-128">Windows Internet Reference</span><span class="sxs-lookup"><span data-stu-id="b4a89-128">Windows Internet Reference</span></span>](wininet-reference.md)<br/> | <span data-ttu-id="b4a89-129">Справочная документация по Интернет-API Windows.</span><span class="sxs-lookup"><span data-stu-id="b4a89-129">Reference documentation for the Windows Internet API.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="b4a89-130">См. также</span><span class="sxs-lookup"><span data-stu-id="b4a89-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4a89-131">Службы Microsoft Windows HTTP (WinHTTP)</span><span class="sxs-lookup"><span data-stu-id="b4a89-131">Microsoft Windows HTTP Services (WinHTTP)</span></span>](/windows/desktop/WinHttp/winhttp-start-page)
</dt> </dl>

 

