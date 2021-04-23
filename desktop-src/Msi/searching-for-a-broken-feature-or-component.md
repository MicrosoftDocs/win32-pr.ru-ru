---
description: Установщик может повысить устойчивость приложения, автоматически переустановив поврежденные компоненты.
ms.assetid: aa565e34-f89d-4d26-945d-67b439586523
title: Поиск неработающей функции или компонента
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8398d084a543ee4c9491242faa287c60d83a5f7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265040"
---
# <a name="searching-for-a-broken-feature-or-component"></a><span data-ttu-id="c0f60-103">Поиск неработающей функции или компонента</span><span class="sxs-lookup"><span data-stu-id="c0f60-103">Searching for a Broken Feature or Component</span></span>

<span data-ttu-id="c0f60-104">Установщик может повысить [устойчивость](resiliency.md) приложения, автоматически переустановив поврежденные компоненты.</span><span class="sxs-lookup"><span data-stu-id="c0f60-104">The installer can increase application [resiliency](resiliency.md) by automatically reinstalling damaged components.</span></span> <span data-ttu-id="c0f60-105">В частности, установщик переустанавливает компонент или компонент, если обнаружит, что файл или раздел реестра, указанный в ключевом столбце [таблицы Component](component-table.md) , отсутствует.</span><span class="sxs-lookup"><span data-stu-id="c0f60-105">Specifically, the installer reinstalls a component or feature if it finds that the file or registry key specified in the KeyPath column of the [Component table](component-table.md) is missing.</span></span>

<span data-ttu-id="c0f60-106">Если ключевой путь к компоненту компонента поврежден в источнике или если при создании ключевого пути в базе данных возникает ошибка, установщик может попытаться открыть пакет установки и переустановить компонент при каждом активировании ярлыка компонента.</span><span class="sxs-lookup"><span data-stu-id="c0f60-106">If the KeyPath of a feature's component is damaged in the source, or if there is an error in how the KeyPath is authored in the database, the installer may attempt to open an installation package and reinstall the feature each time the feature's shortcut is activated.</span></span>

<span data-ttu-id="c0f60-107">Чтобы определить причину появления повторяющихся попыток переустановки компонента или приложения, проверьте в журнале событий две записи, например следующие.</span><span class="sxs-lookup"><span data-stu-id="c0f60-107">To determine the cause of repeated attempts to reinstall a feature or application, check the Event Log for two entries such as the following.</span></span>

``` syntax
Detection of product 'MyProduct', feature 'MyFeature' failed during
 request for component 'MyComponent'
Detection of product 'MyProduct', feature 'MyFeature', component
 'MyComponent' failed
```

<span data-ttu-id="c0f60-108">В первом сообщении указывается, какой компонент пакета продукта был установлен.</span><span class="sxs-lookup"><span data-stu-id="c0f60-108">The first message states which component in the product's package was being installed.</span></span> <span data-ttu-id="c0f60-109">Это компонент, на который ссылается столбец Component в \_ [таблице ярлыков](shortcut-table.md).</span><span class="sxs-lookup"><span data-stu-id="c0f60-109">This is the component referenced in the Component\_ column of the [Shortcut table](shortcut-table.md).</span></span>

<span data-ttu-id="c0f60-110">Второе сообщение указывает, в каком компоненте произошел сбой обнаружения.</span><span class="sxs-lookup"><span data-stu-id="c0f60-110">The second message states which component is failing detection.</span></span> <span data-ttu-id="c0f60-111">Это компонент с отсутствующим или поврежденным ключевой разделом, который запускает переустановку.</span><span class="sxs-lookup"><span data-stu-id="c0f60-111">This is the component with the missing or damaged KeyPath that's triggering the reinstall.</span></span>

 

 



