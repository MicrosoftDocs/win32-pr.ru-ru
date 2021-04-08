---
title: Иажентспичинпутпропертиес
description: Иажентспичинпутпропертиес
ms.assetid: b93e5b46-b8f8-4ca4-8417-7626b97d8928
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e672b26f97cfbe92bc71d0ceab165e100c3ecf92
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104067239"
---
# <a name="iagentspeechinputpropertiesgethotkey"></a><span data-ttu-id="8c45d-103">Иажентспичинпутпропертиес:: насочетание клавиш</span><span class="sxs-lookup"><span data-stu-id="8c45d-103">IAgentSpeechInputProperties::GetHotKey</span></span>

<span data-ttu-id="8c45d-104">\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]</span><span class="sxs-lookup"><span data-stu-id="8c45d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHotKey(
BSTR * pbszHotCharKey  // address of variable for listening key 
);                        
```

<span data-ttu-id="8c45d-105">Извлекает текущее назначение клавиатуры для ключа прослушивания речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="8c45d-105">Retrieves the current keyboard assignment for the speech input Listening key.</span></span>

-   <span data-ttu-id="8c45d-106">Возвращает значение S \_ , чтобы указать, что операция выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="8c45d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="8c45d-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*пбсзотчаркэй*</span><span class="sxs-lookup"><span data-stu-id="8c45d-107"><span id="pbszHotCharKey"></span><span id="pbszhotcharkey"></span><span id="PBSZHOTCHARKEY"></span>*pbszHotCharKey*</span></span>
</dt> <dd>

<span data-ttu-id="8c45d-108">Адрес BSTR, который получает текущее значение сочетания клавиш, используемое для открытия звукового канала для речевого ввода.</span><span class="sxs-lookup"><span data-stu-id="8c45d-108">Address of a BSTR that receives the current hotkey setting used to open the audio channel for speech input.</span></span>

</dd> </dl>

<span data-ttu-id="8c45d-109">Если функция [**Enable**](iagentspeechinputproperties--getenabled.md) возвращает **значение false**, то при запросе этого параметра возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="8c45d-109">If [**GetEnabled**](iagentspeechinputproperties--getenabled.md) returns **False**, querying this setting raises an error.</span></span>

## <a name="see-also"></a><span data-ttu-id="8c45d-110">См. также:</span><span class="sxs-lookup"><span data-stu-id="8c45d-110">See Also</span></span>

[<span data-ttu-id="8c45d-111">**Иажентспичинпутпропертиес:: enable**</span><span class="sxs-lookup"><span data-stu-id="8c45d-111">**IAgentSpeechInputProperties::GetEnabled**</span></span>](iagentspeechinputproperties--getenabled.md)


 

 




