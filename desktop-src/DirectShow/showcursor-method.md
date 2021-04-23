---
description: Метод Шовкурсор делает курсор видимым, когда объект Мсвебдвд находится в полноэкранном режиме.
ms.assetid: 3a611cc8-7979-473d-bd0f-f4ca43701c63
title: Метод Шовкурсор
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 917c1d0d2724259fc19baf72ab6b3844cddc3419
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894766"
---
# <a name="showcursor-method"></a><span data-ttu-id="6311d-103">Метод Шовкурсор</span><span class="sxs-lookup"><span data-stu-id="6311d-103">ShowCursor Method</span></span>

> [!Note]  
> <span data-ttu-id="6311d-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="6311d-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="6311d-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="6311d-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="6311d-106">`ShowCursor`Метод делает курсор видимым, когда объект **мсвебдвд** находится в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="6311d-106">The `ShowCursor` method makes the cursor visible when the **MSWebDVD** object is in full-screen mode.</span></span>

``` syntax
MSWebDVD.ShowCursor(bShow)
```

## <a name="parameters"></a><span data-ttu-id="6311d-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="6311d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6311d-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*бшов*</span><span class="sxs-lookup"><span data-stu-id="6311d-108"><span id="bShow"></span><span id="bshow"></span><span id="BSHOW"></span>*bShow*</span></span>
</dt> <dd>

<span data-ttu-id="6311d-109">Указывает, следует ли отображать курсор в виде логического значения.</span><span class="sxs-lookup"><span data-stu-id="6311d-109">Specifies whether to show the cursor as a Boolean.</span></span>



| <span data-ttu-id="6311d-110">Значение</span><span class="sxs-lookup"><span data-stu-id="6311d-110">Value</span></span> | <span data-ttu-id="6311d-111">Описание</span><span class="sxs-lookup"><span data-stu-id="6311d-111">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="6311d-112">true</span><span class="sxs-lookup"><span data-stu-id="6311d-112">true</span></span>  | <span data-ttu-id="6311d-113">Отображение курсора</span><span class="sxs-lookup"><span data-stu-id="6311d-113">Show the cursor</span></span>        |
| <span data-ttu-id="6311d-114">false</span><span class="sxs-lookup"><span data-stu-id="6311d-114">false</span></span> | <span data-ttu-id="6311d-115">Не показывать курсор</span><span class="sxs-lookup"><span data-stu-id="6311d-115">Do not show the cursor</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6311d-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6311d-116">Return Value</span></span>

<span data-ttu-id="6311d-117">Нет возвращаемого значения.</span><span class="sxs-lookup"><span data-stu-id="6311d-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6311d-118">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6311d-118">Remarks</span></span>

<span data-ttu-id="6311d-119">Когда дисплей DVD переходит в полноэкранный режим, курсор исчезает в течение 3 – 5 секунд.</span><span class="sxs-lookup"><span data-stu-id="6311d-119">When the DVD display goes into full-screen mode, the cursor disappears within 3 to 5 seconds.</span></span> <span data-ttu-id="6311d-120">Используйте этот метод, чтобы сделать курсор снова видимым, если кнопки управления приложения видимы в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="6311d-120">Use this method to make the cursor visible again if your application's control buttons are visible in full-screen mode.</span></span>

 

 



