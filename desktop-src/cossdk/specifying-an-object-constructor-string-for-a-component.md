---
description: Указание строки конструктора объекта для компонента
ms.assetid: 0c5aaaae-368e-4b3e-a483-b3a23c353e6e
title: Указание строки конструктора объекта для компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ca4604d07a5b750d02a968456d33c9e5bc6bee8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895742"
---
# <a name="specifying-an-object-constructor-string-for-a-component"></a><span data-ttu-id="6a0b9-103">Указание строки конструктора объекта для компонента</span><span class="sxs-lookup"><span data-stu-id="6a0b9-103">Specifying an Object Constructor String for a Component</span></span>

<span data-ttu-id="6a0b9-104">Чтобы указать строку конструктора объекта для компонента, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="6a0b9-104">To specify an object constructor string for a component, use the following steps:</span></span>

1.  <span data-ttu-id="6a0b9-105">В области сведений средства администрирования "службы компонентов" щелкните правой кнопкой мыши компонент, который необходимо настроить, и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="6a0b9-105">In the details pane of the Component Services administrative tool, right-click the component that you want to configure and then click **Properties**.</span></span>
2.  <span data-ttu-id="6a0b9-106">В диалоговом окне Свойства компонента перейдите на вкладку **Активация** .</span><span class="sxs-lookup"><span data-stu-id="6a0b9-106">In the component properties dialog box, click the **Activation** tab.</span></span>
3.  <span data-ttu-id="6a0b9-107">Чтобы включить использование строки конструктора объектов, установите флажок **включить конструирование объектов** .</span><span class="sxs-lookup"><span data-stu-id="6a0b9-107">To enable use of the object constructor string, select the **Enable object construction** check box.</span></span>
4.  <span data-ttu-id="6a0b9-108">В поле **строка конструктора** введите строку конструирования (например, DSN = аккаунтингсервер).</span><span class="sxs-lookup"><span data-stu-id="6a0b9-108">In the **Constructor string** box, enter the construction string (for example, DSN=AccountingServer).</span></span> <span data-ttu-id="6a0b9-109">Имеется возможность ввести пустую строку.</span><span class="sxs-lookup"><span data-stu-id="6a0b9-109">You have the option of entering an empty string.</span></span>

> [!Note]  
> <span data-ttu-id="6a0b9-110">Строки конструктора объектов не следует использовать для хранения конфиденциальных данных.</span><span class="sxs-lookup"><span data-stu-id="6a0b9-110">Object constructor strings should not be used to store security-sensitive information.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="6a0b9-111">См. также</span><span class="sxs-lookup"><span data-stu-id="6a0b9-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a0b9-112">Основные понятия о строках конструктора объектов COM+</span><span class="sxs-lookup"><span data-stu-id="6a0b9-112">COM+ Object Constructor Strings Concepts</span></span>](com--object-constructor-strings-concepts.md)
</dt> <dt>

[<span data-ttu-id="6a0b9-113">Использование строки конструктора объекта для создания компонента</span><span class="sxs-lookup"><span data-stu-id="6a0b9-113">Using an Object Constructor String to Construct a Component</span></span>](using-an-object-constructor-string-to-construct-a-component.md)
</dt> </dl>

 

 



