---
title: External. showPopup, метод
description: Обратите внимание, что в этом разделе описываются функции, предназначенные для использования в Интернет-магазинах. | External. showPopup, метод
ms.assetid: 17958543-dbed-45a5-9b02-4800a07cb820
keywords:
- showPopup метод Windows Media Player
- showPopup метод Windows Media Player, внешний класс
- Внешний класс проигрыватель Windows Media Player, метод showPopup
topic_type:
- apiref
api_name:
- External.showPopup
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: acaecb559e7df60067e89ec754ec9432233500f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694750"
---
# <a name="externalshowpopup-method"></a><span data-ttu-id="71647-107">External. showPopup, метод</span><span class="sxs-lookup"><span data-stu-id="71647-107">External.showPopup method</span></span>

> [!Note]  
> <span data-ttu-id="71647-108">В этом разделе описываются функции, предназначенные для использования в Интернет-магазинах.</span><span class="sxs-lookup"><span data-stu-id="71647-108">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="71647-109">Использование этой функции вне контекста Интернет-магазина не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="71647-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="71647-110">Метод **showPopup** указывает проигрывателю Windows Media отображать всплывающую веб-страницу; то есть веб-страница, которая отображается в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="71647-110">The **showPopup** method instructs Windows Media Player to display a pop-up webpage; that is, a webpage that appears in a separate window.</span></span>

## <a name="syntax"></a><span data-ttu-id="71647-111">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="71647-111">Syntax</span></span>


```JScript
External.showPopup(
  PopupIndex,
  Parameters
)
```



## <a name="parameters"></a><span data-ttu-id="71647-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="71647-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="71647-113">*Попупиндекс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71647-113">*PopupIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71647-114">**Число** (**Long**), указывающее индекс всплывающей веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="71647-114">**Number** (**long**) that specifies the index of the pop-up webpage.</span></span>

</dd> <dt>

<span data-ttu-id="71647-115">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="71647-115">*Parameters* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="71647-116">**Строка** , добавляемая проигрывателем Windows Media в URL-адрес веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="71647-116">**String** that Windows Media Player appends to the URL of the webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="71647-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="71647-117">Return value</span></span>

<span data-ttu-id="71647-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="71647-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="71647-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="71647-119">Remarks</span></span>

<span data-ttu-id="71647-120">Проигрыватель Windows Media не интерпретирует всплывающий индекс.</span><span class="sxs-lookup"><span data-stu-id="71647-120">The pop-up index is not interpreted by Windows Media Player.</span></span> <span data-ttu-id="71647-121">Индексы, которые определяют всплывающие веб-страницы, создаются Интернет-магазином и имеют значение только в Интернет-магазине.</span><span class="sxs-lookup"><span data-stu-id="71647-121">Indexes that identify pop-up webpages are created by the online store, and have meaning only to the online store.</span></span>

<span data-ttu-id="71647-122">В следующих шагах показано, как проигрыватель Windows Media использует параметры метода **showPopup** для создания URL-адреса всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="71647-122">The following steps show how Windows Media Player uses the parameters of the **showPopup** method to create a URL for the popup window.</span></span>

1.  <span data-ttu-id="71647-123">Скрипт на странице обнаружения вызывает **showPopup**, передавая целое число в *попупиндекс* и строку в *параметрах*.</span><span class="sxs-lookup"><span data-stu-id="71647-123">Script on a discovery page calls **showPopup**, passing an integer in *PopupIndex* and a string in *Parameters*.</span></span>

2.  <span data-ttu-id="71647-124">Проигрыватель Windows Media передает индекс в [ивмпконтентпартнер:: GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) , чтобы получить URL-адрес отображаемой веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="71647-124">Windows Media Player passes the index to [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo) to retrieve the URL of the webpage to be displayed.</span></span>

3.  <span data-ttu-id="71647-125">Проигрыватель Windows Media добавляет *Параметры* к URL-адресу в виде строки запроса.</span><span class="sxs-lookup"><span data-stu-id="71647-125">Windows Media Player appends *Parameters* to the URL as a query string.</span></span> <span data-ttu-id="71647-126">Например, если **GetItemInfo** возвращает " https://www.Proseware.com/Pages/Popup1.htm ", а *Параметры* равны "длгкс = 800&длги = 400&приветствие = Hi", проигрыватель Windows Media создает следующий URL-адрес:</span><span class="sxs-lookup"><span data-stu-id="71647-126">For example, if **GetItemInfo** returns "https://www.Proseware.com/Pages/Popup1.htm" and *Parameters* is equal to "DlgX=800&DlgY=400&Greeting=Hi", Windows Media Player creates the following URL:</span></span>

    https://www.Proseware.com/Pages/Popup1.htm?DlgX=800&DlgY=400&Greeting=Hi

<span data-ttu-id="71647-127">С помощью *параметров* можно указать размер всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="71647-127">You can use *Parameters* to specify the size of the pop-up window.</span></span> <span data-ttu-id="71647-128">Например, если задать для *параметров* значение "длгкс = 800&длги = 400", то всплывающее окно будет иметь размер 800 пикселей на 400 пикселей.</span><span class="sxs-lookup"><span data-stu-id="71647-128">For example, if you set *Parameters* to "DlgX=800&DlgY=400", the pop-up window will have a size of 800 pixels by 400 pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="71647-129">Требования</span><span class="sxs-lookup"><span data-stu-id="71647-129">Requirements</span></span>



| <span data-ttu-id="71647-130">Требование</span><span class="sxs-lookup"><span data-stu-id="71647-130">Requirement</span></span> | <span data-ttu-id="71647-131">Значение</span><span class="sxs-lookup"><span data-stu-id="71647-131">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="71647-132">Версия</span><span class="sxs-lookup"><span data-stu-id="71647-132">Version</span></span><br/> | <span data-ttu-id="71647-133">Проигрыватель Windows Media 11</span><span class="sxs-lookup"><span data-stu-id="71647-133">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="71647-134">DLL</span><span class="sxs-lookup"><span data-stu-id="71647-134">DLL</span></span><br/>     | <dl> <span data-ttu-id="71647-135"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="71647-135"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71647-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="71647-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71647-137">**Внешний объект для Интернет-магазинов типа 1**</span><span class="sxs-lookup"><span data-stu-id="71647-137">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





