---
description: Статические свойства можно локализовать с помощью частичных карт значений.
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: Локализация статических свойств
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "104356163"
---
# <a name="localizing-static-properties"></a><span data-ttu-id="5b513-103">Локализация статических свойств</span><span class="sxs-lookup"><span data-stu-id="5b513-103">Localizing Static Properties</span></span>

<span data-ttu-id="5b513-104">Статические свойства можно локализовать с помощью частичных карт значений.</span><span class="sxs-lookup"><span data-stu-id="5b513-104">You can localize static properties by using partial value maps.</span></span>

<span data-ttu-id="5b513-105">Следующая процедура описывает, как можно локализовать статические свойства с помощью частичных карт значений с регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="5b513-105">The following procedure describes how static properties can be localized using partial value maps with regular expressions.</span></span>

<span data-ttu-id="5b513-106">**Использование карт значений для локализации статических свойств**</span><span class="sxs-lookup"><span data-stu-id="5b513-106">**To use value maps to localize static properties**</span></span>

1.  <span data-ttu-id="5b513-107">Создайте главный MOF-файл (Мастервм. MOF).</span><span class="sxs-lookup"><span data-stu-id="5b513-107">Create a master MOF file (Mastervm.mof).</span></span>

    <span data-ttu-id="5b513-108">Следующий пример кода можно использовать для создания главного MOF-файла (Мастервм. MOF).</span><span class="sxs-lookup"><span data-stu-id="5b513-108">The following code example can be used to create a master MOF file (Mastervm.mof).</span></span>

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  <span data-ttu-id="5b513-109">Создайте языковые версии MOF-файла, зависящие от языка и языка.</span><span class="sxs-lookup"><span data-stu-id="5b513-109">Create the language-neutral and language-specific versions of the MOF file.</span></span>

    <span data-ttu-id="5b513-110">Введите следующую команду в командной строке, чтобы создать языковые версии MOF-файла, зависящие от языка и языка.</span><span class="sxs-lookup"><span data-stu-id="5b513-110">Type the following command at a command prompt to create the language-neutral and language-specific versions of the MOF file.</span></span>

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    <span data-ttu-id="5b513-111">Компилятор MOF создает зависящие от языка и языковые файлы MOF, Лнвм. mof и ЛСВМ. МФЛ.</span><span class="sxs-lookup"><span data-stu-id="5b513-111">The MOF compiler generates the language-specific and language-neutral MOF files, LnVm.mof and LsVm.mfl.</span></span> <span data-ttu-id="5b513-112">Значения американского английского для свойства [numbers](numbers.md) помещаются в МФЛ-файл для пространства имен американский English.</span><span class="sxs-lookup"><span data-stu-id="5b513-112">The American English values for the [Numbers](numbers.md) property is placed in the .mfl file for the American English namespace.</span></span>

    <span data-ttu-id="5b513-113">В следующем примере кода показано содержимое файла ЛСВМ. МФЛ.</span><span class="sxs-lookup"><span data-stu-id="5b513-113">The following code example shows the contents of the LsVm.mfl file.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  <span data-ttu-id="5b513-114">Скомпилируйте два MOF-файла и сохраните сведения о классах в репозитории CIM.</span><span class="sxs-lookup"><span data-stu-id="5b513-114">Compile the two MOF files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="5b513-115">Введите следующую команду в командной строке, чтобы скомпилировать два MOF-файла.</span><span class="sxs-lookup"><span data-stu-id="5b513-115">Type the following command at a command prompt to compile the two MOF files.</span></span>

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  <span data-ttu-id="5b513-116">Локализовать файл МФЛ для других языков.</span><span class="sxs-lookup"><span data-stu-id="5b513-116">Localize the MFL file for other locales.</span></span>

    <span data-ttu-id="5b513-117">В следующем примере кода показано содержимое файла МФЛ для пространства имен на французском языке.</span><span class="sxs-lookup"><span data-stu-id="5b513-117">The following code example shows the contents of an MFL file for the French namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

<span data-ttu-id="5b513-118">В итоге, отображаемое имя и значение свойства [numbers](numbers.md) зависят от языкового стандарта вошедшего в систему пользователя.</span><span class="sxs-lookup"><span data-stu-id="5b513-118">The net result is that both the display name and the value of the [Numbers](numbers.md) property depend on the locale of the logged-on user.</span></span> <span data-ttu-id="5b513-119">Если пользователь указывает языковой стандарт, который не был предоставлен, то данные квалификатора по умолчанию поступают из пространства имен English (MS \_ 409).</span><span class="sxs-lookup"><span data-stu-id="5b513-119">If the user specifies a locale that has not been provided, the default qualifier data comes from the English (ms\_409) namespace.</span></span>

<span data-ttu-id="5b513-120">Это подразумевает, что каждое строковое значение используется в качестве идентификатора поиска, который не может быть локализован.</span><span class="sxs-lookup"><span data-stu-id="5b513-120">The implication of this design is that each string value is used as a lookup identifier, which cannot be localized.</span></span> <span data-ttu-id="5b513-121">При определении этой схемы необходимо убедиться, что значение, которое поставщик помещает в, не зависит от языкового стандарта.</span><span class="sxs-lookup"><span data-stu-id="5b513-121">When defining this scheme, you must ensure that the value the provider puts in is locale-independent.</span></span>

> [!Note]  
> <span data-ttu-id="5b513-122">В настоящее время Инструментарий WMI не обеспечивает поддержку времени выполнения для сопоставления значений со строками, определенными квалификаторами.</span><span class="sxs-lookup"><span data-stu-id="5b513-122">WMI does not currently provide run-time support for mapping values to strings defined by qualifiers.</span></span> <span data-ttu-id="5b513-123">Интерпретация предлагаемого синтаксиса является обязанностью приложения.</span><span class="sxs-lookup"><span data-stu-id="5b513-123">Interpretation of the suggested syntax is the application's responsibility.</span></span>

 

 

 



