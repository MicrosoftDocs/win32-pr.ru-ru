---
title: Файл конфигурации приложения (ACF)
description: Могут быть аспекты распределенного приложения, влияющие на один компонент, но не имеющие никакого отношения к другому.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF MIDL
- Язык MIDL MIDL, описание, файл конфигурации приложения
- файл конфигурации приложения MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105650290"
---
# <a name="application-configuration-file-acf"></a><span data-ttu-id="65943-106">Файл конфигурации приложения (ACF)</span><span class="sxs-lookup"><span data-stu-id="65943-106">Application Configuration File (ACF)</span></span>

<span data-ttu-id="65943-107">Могут быть аспекты распределенного приложения, влияющие на один компонент, но не имеющие никакого отношения к другому.</span><span class="sxs-lookup"><span data-stu-id="65943-107">There may be aspects of your distributed application that affect one component, but have nothing to do with another.</span></span> <span data-ttu-id="65943-108">Например, объект может содержать большую, сложную структуру данных и передавать содержимое этой структуры данных другому объекту.</span><span class="sxs-lookup"><span data-stu-id="65943-108">For example, an object may contain a large, complex data structure and pass the contents of this data structure to another object.</span></span> <span data-ttu-id="65943-109">Точный макет этой структуры данных может быть бессмысленным для принимающего приложения.</span><span class="sxs-lookup"><span data-stu-id="65943-109">The exact layout of this data structure may be meaningless to the receiving application.</span></span> <span data-ttu-id="65943-110">Кроме того, структура может содержать типы данных, которые компилятор MIDL не распознает и не может создать упаковку и деупаковку кода.</span><span class="sxs-lookup"><span data-stu-id="65943-110">Also, the structure may contain data types that the MIDL compiler does not recognize and cannot generate marshaling and unmarshaling code.</span></span>

<span data-ttu-id="65943-111">Клиентские приложения могут совместно использовать один и тот же интерфейс, но работать на разных платформах; для них может потребоваться собственный набор подпрограмм упаковки.</span><span class="sxs-lookup"><span data-stu-id="65943-111">Client applications may share the same interface but run on different platforms; they may each need their own set of marshaling routines.</span></span> <span data-ttu-id="65943-112">Наконец, отдельным клиентам может не требоваться один и тот же набор функций.</span><span class="sxs-lookup"><span data-stu-id="65943-112">Finally, individual clients may not always need the same set of functions.</span></span> <span data-ttu-id="65943-113">Создание кода-заглушки для функций, которые никогда не будут реализованы в конкретном клиентском приложении, неэффективно.</span><span class="sxs-lookup"><span data-stu-id="65943-113">It is inefficient to generate stub code for functions that will never be implemented in a particular client application.</span></span>

<span data-ttu-id="65943-114">Определив локальные аспекты интерфейса в файле конфигурации приложения (ACF), можно разделить различия между интерфейсами клиента из их сетевого представления, позволяя серверу отправлять и получать данные в согласованном формате, а также делать код заглушки более компактным и эффективным.</span><span class="sxs-lookup"><span data-stu-id="65943-114">By defining these local aspects of your interface in an application configuration file (ACF), you can separate the differences between the client interfaces from their network representation, allowing the server to send and receive data in a consistent format, and making your stub code more compact and efficient.</span></span>

<span data-ttu-id="65943-115">Структура и синтаксис определения интерфейса ACF идентичны определению IDL:</span><span class="sxs-lookup"><span data-stu-id="65943-115">The structure and syntax of an ACF interface definition are identical to the IDL definition:</span></span>

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

<span data-ttu-id="65943-116">По умолчанию имя интерфейса ACF должно соответствовать его имени в определении IDL.</span><span class="sxs-lookup"><span data-stu-id="65943-116">By default, the ACF interface name must match its name in the IDL definition.</span></span> <span data-ttu-id="65943-117">Однако при использовании параметра компилятора MIDL/ [**ACF**](-acf.md) для явного указания имени файла ACF имена интерфейсов не должны совпадать.</span><span class="sxs-lookup"><span data-stu-id="65943-117">However, when you use the MIDL compiler option / [**acf**](-acf.md) to explicitly specify an ACF file name, the interface names do not have to match.</span></span> <span data-ttu-id="65943-118">Эта функция позволяет нескольким интерфейсам совместно использовать одну спецификацию ACF.</span><span class="sxs-lookup"><span data-stu-id="65943-118">This feature allows several interfaces to share a single ACF specification.</span></span>

 

 




