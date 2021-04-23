---
title: Страницы свойств для использования с описателем экрана
description: Домен Active Directory Services предоставляют механизм для добавления страниц на страницу свойств, отображаемую для объекта каталога из Active Directory административных оснасток или оболочки Windows.
ms.assetid: c1dd84e2-50f9-4903-a4b5-4473515e4d0e
ms.tgt_platform: multiple
keywords:
- Отображение описателей AD, страниц свойств для использования с
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c204f4d378e66cda5bc02684cb51cc707ba3d6f2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/17/2020
ms.locfileid: "103890395"
---
# <a name="property-pages-for-use-with-display-specifiers"></a><span data-ttu-id="963fc-104">Страницы свойств для использования с описателем экрана</span><span class="sxs-lookup"><span data-stu-id="963fc-104">Property Pages for Use with Display Specifiers</span></span>

<span data-ttu-id="963fc-105">Домен Active Directory Services предоставляют механизм для добавления страниц на страницу свойств, отображаемую для объекта каталога из Active Directory административных оснасток или оболочки Windows.</span><span class="sxs-lookup"><span data-stu-id="963fc-105">Active Directory Domain Services provide a mechanism for adding pages to the property sheet displayed for a directory object from the Active Directory administrative snap-ins or the Windows shell.</span></span> <span data-ttu-id="963fc-106">Чтобы добавить страницу к странице свойств, реализуйте расширение страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="963fc-106">To add a page to the property sheet, implement a property sheet extension.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="963fc-107">Аудитория разработчиков</span><span class="sxs-lookup"><span data-stu-id="963fc-107">Developer Audience</span></span>

<span data-ttu-id="963fc-108">В этой документации предполагается, что читатель знаком с разработкой COM-операций и компонентов с помощью C++.</span><span class="sxs-lookup"><span data-stu-id="963fc-108">This documentation assumes that the reader is familiar with COM operation and component development using C++.</span></span> <span data-ttu-id="963fc-109">В настоящее время невозможно создать Active Directory расширение вкладки свойств с помощью Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="963fc-109">It is not currently possible to create an Active Directory property sheet extension using Visual Basic.</span></span>

## <a name="creating-an-active-directory-property-sheet-extension"></a><span data-ttu-id="963fc-110">Создание расширения страницы свойств Active Directory</span><span class="sxs-lookup"><span data-stu-id="963fc-110">Creating an Active Directory Property Sheet Extension</span></span>

<span data-ttu-id="963fc-111">*Расширение страницы свойств* — это ВНУТРИПРОЦЕССНЫЙ сервер COM, который реализует определенные интерфейсы и регистрируется в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="963fc-111">A *property sheet extension* is a COM in-proc server that implements certain interfaces and is registered with Active Directory Domain Services.</span></span> <span data-ttu-id="963fc-112">Чтобы создать расширение таблицы свойств, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="963fc-112">To create a property sheet extension, perform the following steps.</span></span>

<span data-ttu-id="963fc-113">**Создание расширения страницы свойств Active Directory**</span><span class="sxs-lookup"><span data-stu-id="963fc-113">**To create an Active Directory property sheet extension**</span></span>

1.  <span data-ttu-id="963fc-114">Создайте библиотеку DLL расширения для таблицы свойств.</span><span class="sxs-lookup"><span data-stu-id="963fc-114">Create the property sheet extension DLL.</span></span> <span data-ttu-id="963fc-115">Расширение страницы свойств — это внутрипроцессный сервер COM, который, как минимум, реализует интерфейсы [**ишеллекстинит**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) и [**ишеллпропшитекст**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) .</span><span class="sxs-lookup"><span data-stu-id="963fc-115">A property sheet extension is a COM in-proc server that, at a minimum, implements the [**IShellExtInit**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellextinit) and [**IShellPropSheetExt**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellpropsheetext) interfaces.</span></span> <span data-ttu-id="963fc-116">Дополнительные сведения см. [в разделе реализация COM-объекта страницы свойств](implementing-the-property-page-com-object.md).</span><span class="sxs-lookup"><span data-stu-id="963fc-116">For more information, see [Implementing the Property Page COM Object](implementing-the-property-page-com-object.md).</span></span>
2.  <span data-ttu-id="963fc-117">Установите расширение страницы свойств на компьютерах, где будет использоваться расширение страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="963fc-117">Install the property sheet extension on the computers where the property sheet extension is to be used.</span></span> <span data-ttu-id="963fc-118">Для этого создайте пакет Microsoft установщик Windows для библиотеки DLL расширения таблицы свойств и разверните пакет соответствующим образом с помощью групповой политики.</span><span class="sxs-lookup"><span data-stu-id="963fc-118">To do this, create a Microsoft Windows Installer package for the property sheet extension DLL and deploy the package appropriately using the group policy.</span></span> <span data-ttu-id="963fc-119">Дополнительные сведения см. в разделе [распространение компонентов пользовательского интерфейса](distributing-user-interface-components.md).</span><span class="sxs-lookup"><span data-stu-id="963fc-119">For more information, see [Distributing User Interface Components](distributing-user-interface-components.md).</span></span>
3.  <span data-ttu-id="963fc-120">Зарегистрируйте расширение страницы свойств в реестре Windows и в службах домен Active Directory.</span><span class="sxs-lookup"><span data-stu-id="963fc-120">Register the property sheet extension in the Windows registry and with Active Directory Domain Services.</span></span> <span data-ttu-id="963fc-121">Дополнительные сведения см. [в разделе Регистрация COM-объекта страницы свойств в описателе экрана](registering-the-property-page-com-object-in-a-display-specifier.md).</span><span class="sxs-lookup"><span data-stu-id="963fc-121">For more information, see [Registering the Property Page COM Object in a Display Specifier](registering-the-property-page-com-object-in-a-display-specifier.md).</span></span>

 

 