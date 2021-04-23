---
title: Иажентспичинпутпропертиес Жетлистенингтип
description: Иажентспичинпутпропертиес Жетлистенингтип
ms.assetid: b0488a54-03f8-43ce-935c-dd49c6ed5dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91218fb7935edb68458d540a8f35fe5402b317ea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700469"
---
# <a name="iagentspeechinputpropertiesgetlisteningtip"></a><span data-ttu-id="a4a4a-103">Иажентспичинпутпропертиес:: Жетлистенингтип</span><span class="sxs-lookup"><span data-stu-id="a4a4a-103">IAgentSpeechInputProperties::GetListeningTip</span></span>

<span data-ttu-id="a4a4a-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a4a4a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetListeningTip(
long * pbListeningTip  // address of variable for listening tip flag
);                       
```

<span data-ttu-id="a4a4a-105">Получает значение, указывающее, включен ли tip прослушивания для вывода.</span><span class="sxs-lookup"><span data-stu-id="a4a4a-105">Retrieves a value indicating whether the Listening Tip is enabled for display.</span></span>

-   <span data-ttu-id="a4a4a-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="a4a4a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="a4a4a-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*пблистенингтип*</span><span class="sxs-lookup"><span data-stu-id="a4a4a-107"><span id="pbListeningTip"></span><span id="pblisteningtip"></span><span id="PBLISTENINGTIP"></span>*pbListeningTip*</span></span>
</dt> <dd>

<span data-ttu-id="a4a4a-108">Адрес переменной, которая получает **значение true** , если TIP прослушивания включен для экрана, или **значение false** , если TIP Listen отключен.</span><span class="sxs-lookup"><span data-stu-id="a4a4a-108">Address of a variable that receives **True** if the Listening Tip is enabled for display, or **False** if the Listening Tip is disabled.</span></span>

</dd> </dl>

<span data-ttu-id="a4a4a-109">Если функция [**Enable**](iagentspeechinputproperties--getenabled.md) возвращает **значение false**, то запросы к любым другим свойствам речевого ввода возвращают ошибку.</span><span class="sxs-lookup"><span data-stu-id="a4a4a-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying any other speech input properties returns an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="a4a4a-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="a4a4a-110">See Also</span></span>

[<span data-ttu-id="a4a4a-111">**Иажентспичинпутпропертиес:: enable**</span><span class="sxs-lookup"><span data-stu-id="a4a4a-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




