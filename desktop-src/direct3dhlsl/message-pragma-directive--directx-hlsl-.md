---
title: Директива pragma сообщения
description: Директива pragma, которая создает сообщения времени компиляции.
ms.assetid: dc3ece10-9730-4ab1-acc8-f95abc92de7d
keywords:
- Директива pragma Message HLSL
topic_type:
- apiref
api_name:
- message pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 813483efb161a06db5ef7e40da99c391f53565bc
ms.sourcegitcommit: 88049609e29f91a42442235885abf56f598b06b3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2021
ms.locfileid: "110153487"
---
# <a name="message-pragma-directive"></a><span data-ttu-id="4abb9-104">Директива pragma сообщения</span><span class="sxs-lookup"><span data-stu-id="4abb9-104">message pragma Directive</span></span>

<span data-ttu-id="4abb9-105">Директива pragma, которая создает сообщения времени компиляции.</span><span class="sxs-lookup"><span data-stu-id="4abb9-105">Pragma directive that produces compiler-time messages.</span></span>



| <span data-ttu-id="4abb9-106">\#сообщение pragma ("*лексема-строка*")</span><span class="sxs-lookup"><span data-stu-id="4abb9-106">\#pragma message("*token-string*")</span></span> |
|-----------------------------------|



 

## <a name="parameters"></a><span data-ttu-id="4abb9-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4abb9-107">Parameters</span></span>



| <span data-ttu-id="4abb9-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="4abb9-108">Item</span></span>                                                                                    | <span data-ttu-id="4abb9-109">Описание:</span><span class="sxs-lookup"><span data-stu-id="4abb9-109">Description</span></span>                  |
|-----------------------------------------------------------------------------------------|------------------------------|
| <span data-ttu-id="4abb9-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*Строка токена*</span><span class="sxs-lookup"><span data-stu-id="4abb9-110"><span id="token-string"></span><span id="TOKEN-STRING"></span>*token-string*</span></span><br/> | <span data-ttu-id="4abb9-111">Сообщение компилятора.</span><span class="sxs-lookup"><span data-stu-id="4abb9-111">Compiler message.</span></span><br/> |



 

## <a name="examples"></a><span data-ttu-id="4abb9-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="4abb9-112">Examples</span></span>

<span data-ttu-id="4abb9-113">В следующем примере демонстрируется обработка сообщений во время предварительной обработки.</span><span class="sxs-lookup"><span data-stu-id="4abb9-113">The following example demonstrates message processing during preprocessing.</span></span>


```
#pragma message "Debugging flag set."
```



## <a name="see-also"></a><span data-ttu-id="4abb9-114">См. также</span><span class="sxs-lookup"><span data-stu-id="4abb9-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4abb9-115">Директивы препроцессора (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4abb9-115">Preprocessor Directives (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[<span data-ttu-id="4abb9-116">\#Директива pragma (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="4abb9-116">\#pragma Directive (DirectX HLSL)</span></span>](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





