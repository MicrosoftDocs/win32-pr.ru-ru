---
description: Функция Шовжаваконсоле является вспомогательной функцией отладки для разработчиков Java. Приложения (или другие программы Java), выполняющиеся в обозревателе Internet Explorer, могут использовать его для вывода сообщений об ошибках и других сведений.
ms.assetid: 070dd833-f8cc-403e-afbf-325648760d5f
title: Функция Шовжаваконсоле
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- extern
api_type:
- DllExport
api_location:
- Msjava.dll
ms.openlocfilehash: 522885bfdd07843549375977630d8d1a7c6776f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105648741"
---
# <a name="showjavaconsole-function"></a><span data-ttu-id="f9ca1-104">Функция Шовжаваконсоле</span><span class="sxs-lookup"><span data-stu-id="f9ca1-104">ShowJavaConsole function</span></span>

<span data-ttu-id="f9ca1-105">Функция **шовжаваконсоле** является вспомогательной функцией отладки для разработчиков Java.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-105">The **ShowJavaConsole** function is a debugging aid for Java developers.</span></span> <span data-ttu-id="f9ca1-106">Приложения (или другие программы Java), выполняющиеся в обозревателе Internet Explorer, могут использовать его для вывода сообщений об ошибках и других сведений.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-106">Applets (or other Java code) running within Internet Explorer can use it to display error messages and other information.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ca1-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9ca1-107">Syntax</span></span>


```C++
void extern ShowJavaConsole(void);
```



## <a name="parameters"></a><span data-ttu-id="f9ca1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9ca1-108">Parameters</span></span>

<span data-ttu-id="f9ca1-109">У этой функции нет параметров.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-109">This function has no parameters.</span></span>

<dl></dl>

## <a name="return-value"></a><span data-ttu-id="f9ca1-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9ca1-110">Return value</span></span>

<span data-ttu-id="f9ca1-111">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-111">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9ca1-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9ca1-112">Remarks</span></span>

<span data-ttu-id="f9ca1-113">Вызов **шовжаваконсоле** приводит к тому, что виртуальная машина Java (VM) отображает окно консоли Java.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-113">Calling **ShowJavaConsole** causes the Java virtual machine (VM) to display the Java console window.</span></span> <span data-ttu-id="f9ca1-114">Окно консоли Java может отображать выходные данные отладки из кода Java, выполняемого в вызывающем процессе.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-114">The Java console window itself can display debugging output from Java code running in the calling process.</span></span> <span data-ttu-id="f9ca1-115">Как правило, это будет использоваться только приложением, на котором размещена виртуальная машина Java.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-115">Typically, this would be used only by an application hosting the Java VM.</span></span> <span data-ttu-id="f9ca1-116">Для каждого процесса существует только одно окно консоли Java; несколько вызовов API приводят к отображению одного и того же окна.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-116">There is only a single Java console window per process; multiple calls to the API result in the same window being displayed.</span></span> <span data-ttu-id="f9ca1-117">Иными словами, если окно консоли уже отображается, ничего не происходит; Если окно не было отображено или пользователь закрыл его, откроется окно.</span><span class="sxs-lookup"><span data-stu-id="f9ca1-117">In other words, if the console window is already displayed, nothing happens; if the window has not been displayed, or the user has closed it, then the window pops up.</span></span>

<span data-ttu-id="f9ca1-118">Эта функция не имеет связанной библиотеки импорта или файла заголовка. его необходимо вызвать с помощью функций [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) и [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) .</span><span class="sxs-lookup"><span data-stu-id="f9ca1-118">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ca1-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f9ca1-119">Requirements</span></span>



| <span data-ttu-id="f9ca1-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f9ca1-120">Requirement</span></span> | <span data-ttu-id="f9ca1-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f9ca1-121">Value</span></span> |
|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ca1-122">DLL</span><span class="sxs-lookup"><span data-stu-id="f9ca1-122">DLL</span></span><br/> | <dl> <span data-ttu-id="f9ca1-123"><dt>Msjava.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9ca1-123"><dt>Msjava.dll</dt></span></span> </dl> |



 

 
