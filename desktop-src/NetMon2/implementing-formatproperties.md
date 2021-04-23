---
description: Сетевой монитор вызывает функцию Форматпропертиес для форматирования данных, отображаемых в области сведений пользовательского интерфейса сетевой монитор.
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: Реализация Форматпропертиес
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144647"
---
# <a name="implementing-formatproperties"></a><span data-ttu-id="a9f4b-103">Реализация Форматпропертиес</span><span class="sxs-lookup"><span data-stu-id="a9f4b-103">Implementing FormatProperties</span></span>

<span data-ttu-id="a9f4b-104">Сетевой монитор вызывает функцию [**форматпропертиес**](formatproperties.md) для форматирования данных, отображаемых в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-104">Network Monitor calls the [**FormatProperties**](formatproperties.md) function to format the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="a9f4b-105">Как правило, **форматпропертиес** вызывается для форматирования строки сводки по протоколу, а затем для форматирования всех экземпляров свойств протокола внутри фрейма.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-105">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="a9f4b-106">Однако сетевой монитор не определяет, сколько раз вызывается **форматпропертиес** для конкретного средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-106">However, Network Monitor does not identify the number of times that **FormatProperties** is called for a specific parser.</span></span>

<span data-ttu-id="a9f4b-107">При вызове [**форматпропертиес**](formatproperties.md)сетевой монитор предоставляет структуру [**пропертинст**](propertyinst.md) для каждого отображаемого свойства.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-107">When calling [**FormatProperties**](formatproperties.md), Network Monitor provides a [**PROPERTYINST**](propertyinst.md) structure for each property that it displays.</span></span> <span data-ttu-id="a9f4b-108">Структура **пропертинст** предоставляет сведения о отображаемых данных, включая указатель на структуру [**PROPERTYINFO**](propertyinfo.md) , указывающую функцию, используемую для форматирования отображаемого свойства данных.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-108">The **PROPERTYINST** structure provides information about the data to be displayed, including a pointer to the [**PROPERTYINFO**](propertyinfo.md) structure that specifies the function to use to format the displayed data property.</span></span>

> [!Note]  
> <span data-ttu-id="a9f4b-109">Структура [**PROPERTYINFO**](propertyinfo.md) указывается при добавлении свойства в [*базу данных свойств*](p.md) средства синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-109">A [**PROPERTYINFO**](propertyinfo.md) structure is specified when adding a property to the [*property database*](p.md) of the parser.</span></span>

 

<span data-ttu-id="a9f4b-110">Сетевой монитор идентифицирует функцию Format для вызова для каждого экземпляра свойства.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-110">Network Monitor identifies the format function to call for each property instance.</span></span> <span data-ttu-id="a9f4b-111">Элемент **инстанцедата** структуры [**PROPERTYINFO**](propertyinfo.md) может указывать следующее:</span><span class="sxs-lookup"><span data-stu-id="a9f4b-111">The **InstanceData** member of the [**PROPERTYINFO**](propertyinfo.md) structure can specify the following:</span></span>

-   <span data-ttu-id="a9f4b-112">Функция [**форматпропертинстанце**](formatpropertyinstance.md) для использования [*универсального модуля форматирования*](g.md) , предоставляемого сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-112">The [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the [*generic formatter*](g.md) that Network Monitor provides.</span></span>

    <span data-ttu-id="a9f4b-113">— или —</span><span class="sxs-lookup"><span data-stu-id="a9f4b-113">– or –</span></span>

-   <span data-ttu-id="a9f4b-114">Имя функции пользовательского формата, предоставляемой анализатором.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-114">The name of a custom format function that the parser provides.</span></span>

<span data-ttu-id="a9f4b-115">Функции [**форматпропертинстанце**](formatpropertyinstance.md) и пользовательского формата возвращают отформатированные данные, отображаемые в области сведений пользовательского интерфейса сетевой монитор.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-115">The [**FormatPropertyInstance**](formatpropertyinstance.md) and the custom format functions return the formatted data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="a9f4b-116">На следующем рисунке показано, как сетевой монитор идентифицирует функцию, вызываемую для каждого экземпляра свойства.</span><span class="sxs-lookup"><span data-stu-id="a9f4b-116">The following illustration shows how Network Monitor identifies the function to call for each property instance.</span></span>

![как сетевой монитор определяет вызываемую функцию](images/formatprop1.png)

<span data-ttu-id="a9f4b-118">Следующая процедура определяет шаги, необходимые для реализации [**форматпропертиес**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="a9f4b-118">The following procedure identifies the steps necessary to implement [**FormatProperties**](formatproperties.md).</span></span>

<span data-ttu-id="a9f4b-119">**Реализация Форматпропертиес**</span><span class="sxs-lookup"><span data-stu-id="a9f4b-119">**To implement FormatProperties**</span></span>

-   <span data-ttu-id="a9f4b-120">Используя структуру цикла, вызовите функцию Format для каждой структуры [**пропертинст**](propertyinst.md) , которая передается средству синтаксического анализа в параметре *лппропинст* функции [**форматпропертиес**](formatproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f4b-120">Using a loop structure, call the format function for each [**PROPERTYINST**](propertyinst.md) structure that is passed to the parser in the *lpPropInst* parameter of the [**FormatProperties**](formatproperties.md) function.</span></span>

<span data-ttu-id="a9f4b-121">Ниже приведена базовая реализация [**форматпропертиес**](formatproperties.md).</span><span class="sxs-lookup"><span data-stu-id="a9f4b-121">The following is a basic implementation of [**FormatProperties**](formatproperties.md).</span></span>

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



