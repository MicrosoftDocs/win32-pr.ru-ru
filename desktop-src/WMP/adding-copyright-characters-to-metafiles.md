---
title: Добавление символов авторского права в метафайлы
description: Символы для авторского права и символов регистрации товарного знака (\ 169; или \ 174;) могут отображаться неправильно, если метафайл не кодируется с помощью схемы кодировки UTF-8.
ms.assetid: 9124c8d4-1fc1-4163-ada9-d96af58f8b98
keywords:
- Добавление символов авторского права в метафайлы Windows Media Player
topic_type:
- apiref
api_name:
- Adding Copyright Characters to Metafiles
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e71b116a3500fdb4217613c81bd4f041af75a66
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/25/2019
ms.locfileid: "104333968"
---
# <a name="adding-copyright-characters-to-metafiles"></a><span data-ttu-id="47bec-104">Добавление символов авторского права в метафайлы</span><span class="sxs-lookup"><span data-stu-id="47bec-104">Adding Copyright Characters to Metafiles</span></span>

<span data-ttu-id="47bec-105">Символы для авторского права и символов регистрации товарного знака (© или®) могут отображаться неправильно, если метафайл не кодируется с помощью схемы кодировки UTF-8.</span><span class="sxs-lookup"><span data-stu-id="47bec-105">The characters for copyright and trademark registration symbols ( © or ® ) may not display correctly if the metafile is not encoded using the UTF-8 encoding scheme.</span></span> <span data-ttu-id="47bec-106">В этом случае для правильного отображения любого из этих символов для всех пользователей можно использовать эквиваленты ASCII (c) и (r) внутри элемента **Copyright** , как показано в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="47bec-106">In this case, to display either of these symbols properly for all users, you can use the ASCII equivalents (c) and (r) inside the **COPYRIGHT** element, as shown in the following code.</span></span>


```
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>
```



<span data-ttu-id="47bec-107">Если метафайл кодируется с помощью UTF-8, то авторские знаки и символы товарных знаков будут отображаться правильно.</span><span class="sxs-lookup"><span data-stu-id="47bec-107">If the metafile is encoded using UTF-8, copyright and trademark symbols will display correctly.</span></span>

## <a name="see-also"></a><span data-ttu-id="47bec-108">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="47bec-108">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47bec-109">**Справочник по элементам метафайлов Windows Media**</span><span class="sxs-lookup"><span data-stu-id="47bec-109">**Windows Media Metafile Elements Reference**</span></span>](windows-media-metafile-elements-reference.md)
</dt> </dl>

 

 




