---
title: Отображение диалоговых окон
description: Отображение диалоговых окон
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Интернет-магазины проигрывателя Windows Media, отображение диалоговых окон
- Интернет-магазины, отображение диалоговых окон
- Тип 1 Интернет-магазины, отображение диалоговых окон
- Интернет-магазины проигрывателя Windows Media, диалоговые окна
- Интернет-магазины, диалоговые окна
- Тип 1 Интернет-магазинов, диалоговые окна
- Отображение диалоговых окон
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ebe008a6c3eac872edea497dc9d50da408aa7eb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103788773"
---
# <a name="displaying-dialog-boxes"></a><span data-ttu-id="47a14-110">Отображение диалоговых окон</span><span class="sxs-lookup"><span data-stu-id="47a14-110">Displaying Dialog Boxes</span></span>

<span data-ttu-id="47a14-111">Интернет-магазин может вызвать диалоговые окна с помощью проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="47a14-111">The online store can invoke dialog boxes through Windows Media Player.</span></span> <span data-ttu-id="47a14-112">Для этого вызовите [External. showPopup](external-showpopup.md) из кода скрипта страницы обнаружения, указав пользовательское значение индекса, представляющее отображаемое диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="47a14-112">To do this, call [External.showPopup](external-showpopup.md) from the discovery page script code, providing a custom index value that represents the dialog box to display.</span></span> <span data-ttu-id="47a14-113">Это значение индекса имеет смысл только для кода Интернет-магазина. Проигрыватель Windows Media не интерпретирует это значение.</span><span class="sxs-lookup"><span data-stu-id="47a14-113">This index value has meaning only to the online store code; Windows Media Player does not interpret this value.</span></span> <span data-ttu-id="47a14-114">Проигрыватель Windows Media вызывает [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), передавая g \_ сзитеминфо \_ попупурл для параметра *бстринфонаме* и номер индекса для параметра *пконтекст* .</span><span class="sxs-lookup"><span data-stu-id="47a14-114">Windows Media Player then calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_PopupURL for the *bstrInfoName* parameter and the index number for the *pContext* parameter.</span></span> <span data-ttu-id="47a14-115">Затем подключаемый модуль возвращает **строку BSTR** , содержащую URL-адрес веб-страницы, отображаемой в диалоговом окне, а проигрыватель отображает диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="47a14-115">The plug-in then returns a **BSTR** containing the URL of the webpage to display in the dialog box and the Player shows the dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47a14-116">См. также</span><span class="sxs-lookup"><span data-stu-id="47a14-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47a14-117">**Справка по программированию для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="47a14-117">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




