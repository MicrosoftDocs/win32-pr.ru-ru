---
description: Псевдоним в WMI является символьной ссылкой либо в классе, либо в экземпляре класса, расположенном в любом месте файла MOF-файл (MOF).
ms.assetid: bf4981dc-3aab-46c5-bf02-48132ccec8c2
ms.tgt_platform: multiple
title: Создание псевдонима WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fdd538e113f227eac4980855ea0035e839b92fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105702078"
---
# <a name="creating-a-wmi-alias"></a><span data-ttu-id="f0c59-103">Создание псевдонима WMI</span><span class="sxs-lookup"><span data-stu-id="f0c59-103">Creating a WMI Alias</span></span>

<span data-ttu-id="f0c59-104">[*Псевдоним*](gloss-a.md) в WMI является символьной ссылкой либо в классе, либо в экземпляре класса, расположенном в любом месте файла MOF-файл (MOF).</span><span class="sxs-lookup"><span data-stu-id="f0c59-104">An [*alias*](gloss-a.md) in WMI is a symbolic reference in either a class or a class instance located elsewhere in a Managed Object Format (MOF) file.</span></span> <span data-ttu-id="f0c59-105">Компилятор MOF использует Псевдонимы для установки ссылок между классами и экземплярами.</span><span class="sxs-lookup"><span data-stu-id="f0c59-105">The MOF compiler uses aliases to establish references between classes and instances.</span></span> <span data-ttu-id="f0c59-106">Компилятор разрешает псевдонимы для классов, на которые они ссылаются, поэтому имена псевдонимов недоступны в скомпилированном коде.</span><span class="sxs-lookup"><span data-stu-id="f0c59-106">The compiler resolves aliases to the classes to which they refer, so alias names are not available in compiled code.</span></span> <span data-ttu-id="f0c59-107">В результате клиентские приложения не могут ссылаться на классы, использующие псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="f0c59-107">As a result, client applications cannot refer to classes using aliases.</span></span>

> [!Note]  
> <span data-ttu-id="f0c59-108">Инструментарий WMI поддерживает переадресацию ссылок, но не циклические псевдонимы.</span><span class="sxs-lookup"><span data-stu-id="f0c59-108">WMI supports forward referencing but not circular aliases.</span></span>

 

<span data-ttu-id="f0c59-109">Псевдоним имеет область только в MOF-файле, в котором объявляется псевдоним.</span><span class="sxs-lookup"><span data-stu-id="f0c59-109">An alias has scope only within the MOF file in which you declare the alias.</span></span> <span data-ttu-id="f0c59-110">Поэтому в качестве ярлыка для длинного пути к объекту обычно используется псевдоним.</span><span class="sxs-lookup"><span data-stu-id="f0c59-110">Therefore, you typically use an alias as a shortcut to a lengthy object path.</span></span>

<span data-ttu-id="f0c59-111">**Определение псевдонима**</span><span class="sxs-lookup"><span data-stu-id="f0c59-111">**To define an alias**</span></span>

1.  <span data-ttu-id="f0c59-112">Добавьте фразу "AS $*aliasname*" в объявление экземпляра или класса.</span><span class="sxs-lookup"><span data-stu-id="f0c59-112">Add the phrase "as $*aliasname*" to the instance or class declaration.</span></span>
2.  <span data-ttu-id="f0c59-113">Имена псевдонимов следуют тем же правилам, что и имена экземпляров и классов, за исключением того, что имена псевдонимов должны начинаться со знака доллара ($).</span><span class="sxs-lookup"><span data-stu-id="f0c59-113">Alias names follow the same rules as instance and class names, except that alias names must begin with a dollar sign ($).</span></span> <span data-ttu-id="f0c59-114">Символы подчеркивания могут присутствовать в имени псевдонима после исходного символа.</span><span class="sxs-lookup"><span data-stu-id="f0c59-114">Underscores can appear in an alias name following the initial character.</span></span>

<span data-ttu-id="f0c59-115">В следующем примере кода показано, как использовать псевдоним в определении класса.</span><span class="sxs-lookup"><span data-stu-id="f0c59-115">The following code example describes how to use an alias in a class definition.</span></span>

``` syntax
class MyClass as $MyClassAlias
{
};
instance of MyClass as $MyInstanceAlias
{
};
```

<span data-ttu-id="f0c59-116">В следующих примерах кода описывается использование псевдонима в качестве символьной ссылки на путь к объекту.</span><span class="sxs-lookup"><span data-stu-id="f0c59-116">The following code examples describe how to use an alias as a symbolic reference to an object path.</span></span> <span data-ttu-id="f0c59-117">В этих примерах объявляются два класса для описания диска: класс диска, указывающий букву диска, и класс Дискреф для указания пути к диску.</span><span class="sxs-lookup"><span data-stu-id="f0c59-117">These examples declare two classes to describe a disk: the Disk class to indicate the drive letter and the DiskRef class to indicate the disk path.</span></span> <span data-ttu-id="f0c59-118">Псевдоним определяется для экземпляра класса диска.</span><span class="sxs-lookup"><span data-stu-id="f0c59-118">An alias is defined for the Disk class instance.</span></span> <span data-ttu-id="f0c59-119">Этот псевдоним используется в качестве значения свойства Пастодиск в экземпляре Дискреф.</span><span class="sxs-lookup"><span data-stu-id="f0c59-119">This alias is used as the value for the PathToDisk property in the DiskRef instance.</span></span>

``` syntax
class Disk {
    [key]  string    DriveLetter;
};

class DiskRef 
{
    [key]  string    MyKey;
    Disk   ref       PathToDisk;
};

instance of Disk as $DiskAlias 
{
    DriveLetter = "c";
};

instance of DiskRef
{
    MyKey      =  "hello";
    PathToDisk = $DiskAlias;
};
```

## <a name="related-topics"></a><span data-ttu-id="f0c59-120">См. также</span><span class="sxs-lookup"><span data-stu-id="f0c59-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f0c59-121">Создание класса</span><span class="sxs-lookup"><span data-stu-id="f0c59-121">Creating a Class</span></span>](creating-a-class.md)
</dt> </dl>

 

 



