---
description: ICE97 проверяет, что два компонента не изолируют общий компонент к одному и тому же каталогу.
ms.assetid: 76eeb238-02a1-43c1-a3d7-5178e3c3eaee
title: ICE97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34c41701ce04c0071d6599f888083dfbea4bfc0c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105650904"
---
# <a name="ice97"></a><span data-ttu-id="70c40-103">ICE97</span><span class="sxs-lookup"><span data-stu-id="70c40-103">ICE97</span></span>

<span data-ttu-id="70c40-104">ICE97 проверяет, что два компонента не изолируют общий компонент к одному и тому же каталогу.</span><span class="sxs-lookup"><span data-stu-id="70c40-104">ICE97 verifies that two components do not isolate a shared component to the same directory.</span></span>

## <a name="result"></a><span data-ttu-id="70c40-105">Результат</span><span class="sxs-lookup"><span data-stu-id="70c40-105">Result</span></span>

<span data-ttu-id="70c40-106">ICE97 отправляет следующие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="70c40-106">ICE97 posts the following warnings.</span></span>



| <span data-ttu-id="70c40-107">Предупреждение ICE97</span><span class="sxs-lookup"><span data-stu-id="70c40-107">ICE97 Warning</span></span>                                                                                                                                                                    | <span data-ttu-id="70c40-108">Описание</span><span class="sxs-lookup"><span data-stu-id="70c40-108">Description</span></span>                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span data-ttu-id="70c40-109">Этот компонент \[ 1 \] устанавливает общий компонент в тот же каталог \[ 2 \] , что и другой, что приводит к разрыву правил компонента, если для установки выбраны оба (или более) компонента.</span><span class="sxs-lookup"><span data-stu-id="70c40-109">This component \[1\] installs the Shared component into the same directory \[2\] as another, which breaks component rules if both (or more) components are selected for install.</span></span> | <span data-ttu-id="70c40-110">Два компонента не должны изолировать общий компонент к одному и тому же каталогу.</span><span class="sxs-lookup"><span data-stu-id="70c40-110">Two components must not isolate a shared component to the same directory.</span></span> |



 

<span data-ttu-id="70c40-111">Например, Component1 и Component2, которые совместно используют Компонентшаред, устанавливаются в один и тот же каталог.</span><span class="sxs-lookup"><span data-stu-id="70c40-111">For example, Component1 and Component2, which share ComponentShared, are installed to the same directory.</span></span> <span data-ttu-id="70c40-112">Оба указывают Компонентшаред как изолированный компонент.</span><span class="sxs-lookup"><span data-stu-id="70c40-112">Both specify ComponentShared as an isolated component.</span></span> <span data-ttu-id="70c40-113">Из-за изоляции файлы в Компонентшаред копируются дважды в Справочник по каталогам \_ для Component1 и Component2.</span><span class="sxs-lookup"><span data-stu-id="70c40-113">Because of the isolation, the files in ComponentShared are copied twice into the Directory\_ reference for Component1 and Component2.</span></span> <span data-ttu-id="70c40-114">Теперь компоненты имеют один счетчик ссылок на копии файлов.</span><span class="sxs-lookup"><span data-stu-id="70c40-114">The components now have one reference count on the copy of files.</span></span> <span data-ttu-id="70c40-115">Это нарушает правила компонента установщика.</span><span class="sxs-lookup"><span data-stu-id="70c40-115">This is in violation of the Installer component rules.</span></span> <span data-ttu-id="70c40-116">Если Component1 удаляется, файлы изолированных компонентов удаляются, а Component2 разрывается.</span><span class="sxs-lookup"><span data-stu-id="70c40-116">If Component1 is uninstalled, the isolated components files are removed and Component2 is broken.</span></span>

## <a name="related-topics"></a><span data-ttu-id="70c40-117">См. также</span><span class="sxs-lookup"><span data-stu-id="70c40-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70c40-118">Справочник по ICE</span><span class="sxs-lookup"><span data-stu-id="70c40-118">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



