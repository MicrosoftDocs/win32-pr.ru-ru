---
description: Сетевой монитор использует функцию экспорта DllMain для определения существования средства синтаксического анализа и освобождения ресурсов, которые сетевой монитор использует для хранения сведений о средстве синтаксического анализа.
ms.assetid: 1741a12c-3645-4e83-b97f-37e67218c5eb
title: Реализация средства синтаксического анализа DllMain
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55dd1ab7432920ac7496643c7c6f9aa0692daf56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808687"
---
# <a name="implementing-dllmain-parser"></a><span data-ttu-id="021b4-103">Реализация средства синтаксического анализа DllMain</span><span class="sxs-lookup"><span data-stu-id="021b4-103">Implementing DllMain Parser</span></span>

<span data-ttu-id="021b4-104">Сетевой монитор использует функцию экспорта **DllMain** для определения существования средства синтаксического анализа и освобождения ресурсов, которые сетевой монитор использует для хранения сведений о средстве синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="021b4-104">Network Monitor uses the **DllMain** export function to identify the existence of the parser, and release resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="021b4-105">Когда сетевой монитор вызывает функцию **DllMain** в первый раз, Библиотека DLL средства синтаксического анализа вызывает [**креатепротокол**](createprotocol.md) для выполнения следующих действий:</span><span class="sxs-lookup"><span data-stu-id="021b4-105">When Network Monitor calls **DllMain** for the first time, the parser DLL calls [**CreateProtocol**](createprotocol.md) to do the following:</span></span>

-   <span data-ttu-id="021b4-106">Укажите протокол, который обнаруживает анализатор.</span><span class="sxs-lookup"><span data-stu-id="021b4-106">Specify the protocol that the parser detects.</span></span>
-   <span data-ttu-id="021b4-107">Укажите точки входа для оставшихся функций экспорта средства синтаксического анализа, которые сетевой монитор вызовы.</span><span class="sxs-lookup"><span data-stu-id="021b4-107">Provide entry points for remaining parser export functions that Network Monitor calls.</span></span>

<span data-ttu-id="021b4-108">Когда сетевой монитор вызывает **DllMain** в последний раз, функция **DllMain** вызывает [**дестройпротокол**](destroyprotocol.md) , чтобы освободить все ресурсы, которые сетевой монитор использует для хранения сведений о средстве синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="021b4-108">When Network Monitor calls **DllMain** for the last time, **DllMain** calls [**DestroyProtocol**](destroyprotocol.md) to release all resources that Network Monitor uses to store information about the parser.</span></span>

<span data-ttu-id="021b4-109">Следующая процедура определяет шаги, необходимые для реализации функции **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="021b4-109">The following procedure identifies the steps necessary to implement **DllMain**.</span></span>

<span data-ttu-id="021b4-110">**Реализация функции DllMain**</span><span class="sxs-lookup"><span data-stu-id="021b4-110">**To implement DllMain**</span></span>

1.  <span data-ttu-id="021b4-111">Укажите структуру [**EntryPoint**](entrypoints.md) для функции [**креатепротокол**](createprotocol.md) и переменной глобальной присоединения.</span><span class="sxs-lookup"><span data-stu-id="021b4-111">Specify the [**ENTRYPOINTS**](entrypoints.md) structure for the [**CreateProtocol**](createprotocol.md) function and global Attach variable.</span></span> <span data-ttu-id="021b4-112">Переменная Attach используется для наблюдения за количеством выполняемых экземпляров протокола.</span><span class="sxs-lookup"><span data-stu-id="021b4-112">The Attach variable is used to track the number of protocol instances that are running.</span></span>
2.  <span data-ttu-id="021b4-113">Проверьте значение параметра *команды* , который устанавливает операционная система.</span><span class="sxs-lookup"><span data-stu-id="021b4-113">Look at the value of the *Command* parameter that the operating system sets.</span></span>

    <span data-ttu-id="021b4-114">Если параметру *команды* присвоено значение DLL \_ Process \_ Attach и Attach равно 0, то вызовите [**креатепротокол**](createprotocol.md) , чтобы указать имя протокола и точки входа для следующих функций экспорта.</span><span class="sxs-lookup"><span data-stu-id="021b4-114">If the *Command* parameter is set to DLL\_PROCESS\_ATTACH and Attach is 0, then call [**CreateProtocol**](createprotocol.md) to provide the protocol name and entry points for the following export functions.</span></span>

    -   <span data-ttu-id="021b4-115">**Зарегистрировать**</span><span class="sxs-lookup"><span data-stu-id="021b4-115">**Register**</span></span>
    -   <span data-ttu-id="021b4-116">**Отмена регистрации**</span><span class="sxs-lookup"><span data-stu-id="021b4-116">**Deregister**</span></span>
    -   <span data-ttu-id="021b4-117">**рекогнизефраме**</span><span class="sxs-lookup"><span data-stu-id="021b4-117">**RecognizeFrame**</span></span>
    -   <span data-ttu-id="021b4-118">**аттачпропертиес**</span><span class="sxs-lookup"><span data-stu-id="021b4-118">**AttachProperties**</span></span>
    -   <span data-ttu-id="021b4-119">**Форматпропертиес** (требуется только в том случае, если в сетевой монитор будут отображаться свойства протокола).</span><span class="sxs-lookup"><span data-stu-id="021b4-119">**FormatProperties** (only required if Network Monitor will be displaying the protocol properties).</span></span>

    <span data-ttu-id="021b4-120">Если параметру *команды* присвоено значение \_ DLL \_ отсоединение процесса и присоединение равно 0, то вызовите [**дестройпротокол**](destroyprotocol.md) , используя экземпляр, который [**креатепротокол**](createprotocol.md) возвращает.</span><span class="sxs-lookup"><span data-stu-id="021b4-120">If the *Command* parameter is set to DLL\_PROCESS\_DETACH and Attach is 0, then call [**DestroyProtocol**](destroyprotocol.md) using the instance handle that [**CreateProtocol**](createprotocol.md) returns.</span></span>

3.  <span data-ttu-id="021b4-121">Возвращает **значение true** , поскольку функция синтаксического анализа **DllMain** должна всегда возвращать **значение true**.</span><span class="sxs-lookup"><span data-stu-id="021b4-121">Return **TRUE** because the **DllMain** parser function must always return **TRUE**.</span></span>

<span data-ttu-id="021b4-122">Ниже приведена базовая реализация **DllMain**.</span><span class="sxs-lookup"><span data-stu-id="021b4-122">The following is a basic implementation of **DllMain**.</span></span> <span data-ttu-id="021b4-123">В примере кода используется оператор Case для перехвата значений параметра *Command* , чтобы определить, следует ли вызывать [**креатепротокол**](createprotocol.md) или [**дестройпротокол**](destroyprotocol.md) .</span><span class="sxs-lookup"><span data-stu-id="021b4-123">The code example uses a case statement to trap values of the *Command* parameter to determine if [**CreateProtocol**](createprotocol.md) or [**DestroyProtocol**](destroyprotocol.md) should be called.</span></span>

``` syntax
#include <windows.h>

// Entry point structure for parser export functions and global
// Attach variable.
ENTRYPOINTS EntryPoints =
{
  Register,
  Deregister,
  RecognizeFrame,
  AttachProperties,
  FormatProperties
};

DWORD Attached = 0; 

BOOL WINAPI DllMain(HANDLE hInstance, ULONG Command, LPVOID Reserved)
{
  switch(Command)
  {
  // Call CreateProtocol.
  case DLL_PROCESS_ATTACH:
       // Loading parser DLL.
       if(Attached == 0)
       {
         hProtocol = CreateProtocol( "ProtocolName",
                                     &EntryPoints,
                                     ENTRYPOINTS_SIZE);
       }
       Attached++;
       break;
  // Call DestroyProtocol.
  case DLL_PROCESS_DETACH:
       // Unloading parser DLL.
       Attached--;
       if(Attached == 0)
       {
         DestroyProtocol( hProtocol);
       }
       break;
  }
  return TRUE;
}
```

 

 



