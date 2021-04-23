---
description: В этом разделе описывается настройка среды для использования библиотек COM платформы Tablet PC в C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: Библиотека COM и элементы управления ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b9304880380ea95bc698c52d200931b77f64480
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701348"
---
# <a name="com-library-and-activex-controls"></a><span data-ttu-id="0b83b-103">Библиотека COM и элементы управления ActiveX</span><span class="sxs-lookup"><span data-stu-id="0b83b-103">COM Library and ActiveX Controls</span></span>

<span data-ttu-id="0b83b-104">В этом разделе описывается настройка среды для использования библиотек COM платформы Tablet PC в C++.</span><span class="sxs-lookup"><span data-stu-id="0b83b-104">This section describes how to set up your environment to use the Tablet PC platform COM libraries in C++.</span></span>

## <a name="microsoft-visual-c"></a><span data-ttu-id="0b83b-105">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="0b83b-105">Microsoft Visual C++</span></span>

<span data-ttu-id="0b83b-106">Чтобы создать приложения для планшетных ПК в Visual C++, необходимо обновить системные переменные среды, настроить параметры каталога для Visual Studio и получить доступ к интерфейсам планшетных ПК в проекте.</span><span class="sxs-lookup"><span data-stu-id="0b83b-106">To build Tablet PC applications in Visual C++, you need to update the system environment variables, set up directory options for Visual Studio, and access the Tablet PC interfaces in your project.</span></span>

<span data-ttu-id="0b83b-107">Чтобы обновить переменные среды, следуйте инструкциям, приведенным в Windows SDK для добавления переменных среды в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="0b83b-107">To update the environment variables, follow the instructions provided by the Windows SDK for adding the environment variables to Visual Studio.</span></span>

### <a name="accessing-the-tablet-pc-interfaces"></a><span data-ttu-id="0b83b-108">Доступ к интерфейсам планшетных ПК</span><span class="sxs-lookup"><span data-stu-id="0b83b-108">Accessing the Tablet PC Interfaces</span></span>

<span data-ttu-id="0b83b-109">Для доступа к интерфейсам планшетных ПК необходимо включить в проект файлы Мсинкаут. h и Мсинкаут \_ i. c.</span><span class="sxs-lookup"><span data-stu-id="0b83b-109">To access the Tablet PC interfaces, you must include the Msinkaut.h and Msinkaut\_i.c files in your project.</span></span>


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



<span data-ttu-id="0b83b-110">Можно также использовать следующую директиву импорта вместо \# инструкций include, перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="0b83b-110">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="0b83b-111">Для доступа к интерфейсам Инканалисис необходимо включить в проект файлы Иаком. h и Иаком \_ i. c.</span><span class="sxs-lookup"><span data-stu-id="0b83b-111">To access the InkAnalysis interfaces, you must include IACom.h and IACom\_i.c files in your project.</span></span>


```C++
#include <IACom.h>
#include <IACom_i.c>
```



<span data-ttu-id="0b83b-112">Можно также использовать следующую директиву импорта вместо \# инструкций include, перечисленных выше.</span><span class="sxs-lookup"><span data-stu-id="0b83b-112">You can also use the following import directive instead of the \#include statements previously listed.</span></span>


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="0b83b-113">Для доступа к интерфейсам [**инкдивидер**](inkdivider-class.md) необходимо включить \_ в проект файлы msinkaut15 i. c и msinkaut15. h.</span><span class="sxs-lookup"><span data-stu-id="0b83b-113">To access the [**InkDivider**](inkdivider-class.md) interfaces, you must include msinkaut15\_i.c and msinkaut15.h files in your project.</span></span>

> [!Note]  
> <span data-ttu-id="0b83b-114">Инкдивидер был заменен API-интерфейсами анализа рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="0b83b-114">InkDivider has been superseded by the Ink Analysis APIs.</span></span>

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



<span data-ttu-id="0b83b-115">Можно также использовать следующую директиву импорта вместо \# инструкций include.</span><span class="sxs-lookup"><span data-stu-id="0b83b-115">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



<span data-ttu-id="0b83b-116">Для доступа к интерфейсам [**пенинпутпанел**](peninputpanel-class.md) необходимо включить \_ в проект файлы пенинпутпанел i. c и пенинпутпанел. h.</span><span class="sxs-lookup"><span data-stu-id="0b83b-116">To access the [**PenInputPanel**](peninputpanel-class.md) interfaces, you must include PenInputPanel\_i.c and PenInputPanel.h files in your project.</span></span>


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



<span data-ttu-id="0b83b-117">Можно также использовать следующую директиву импорта вместо \# инструкций include.</span><span class="sxs-lookup"><span data-stu-id="0b83b-117">You can also use the following import directive instead of the \# include statements.</span></span>


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> <span data-ttu-id="0b83b-118">Интерфейсы API Пенинпутпанел были заменены в Windows Vista новыми интерфейсами панели ввода текста.</span><span class="sxs-lookup"><span data-stu-id="0b83b-118">The PenInputPanel APIs have been superseded in Windows Vista by the new Text Input Panel interfaces.</span></span>

 

<span data-ttu-id="0b83b-119">Для доступа к интерфейсам элемента управления [InkEdit](inkedit-control-reference.md) необходимо включить в проект файлы с заданными. h и \_ i. c.</span><span class="sxs-lookup"><span data-stu-id="0b83b-119">To access the [InkEdit](inkedit-control-reference.md) Control interfaces, you must include the Inked.h and Inked\_i.c files in your project.</span></span>


```C++
#include <inked.h>
#include <inked_i.c>
```



<span data-ttu-id="0b83b-120">Кроме того, можно \# импортировать файл InkEd.dll.</span><span class="sxs-lookup"><span data-stu-id="0b83b-120">Alternatively, you can \#import the InkEd.dll file.</span></span>


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



