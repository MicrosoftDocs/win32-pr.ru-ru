---
description: Объясняет, как создать элемент управления для математических входных данных.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Создание элемента управления для математических входных данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee8cca2a799bd44e79ef2f32691614bb3f22c933b40aa23dc4aa0cd6cfb6fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967723"
---
# <a name="creating-a-math-input-control"></a>Создание элемента управления для математических входных данных

Чтобы создать элемент управления математическими данными, необходимо выполнить следующие действия.

-   [Включение заголовков и библиотек для элемента управления математическими данными](#include-headers-and-libraries-for-the-math-input-control)
-   [Объявление указателя управления и вызов CoInitialize для указателя управления](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Отображение элемента управления](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Включение заголовков и библиотек для элемента управления математическими данными

Следующий код следует поместить в верхнюю часть кода, где будет использоваться элемент управления Math.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Этот код добавит поддержку элемента управления Math для ввода в приложение.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Объявление указателя управления и вызов CoInitialize для указателя управления

После включения заголовков для элемента управления можно объявить управляющий указатель и вызвать для него функцию CoInitialize, чтобы создать маркер для интерфейса ввода математических элементов. Следующий код можно поместить в класс или как глобальную переменную в реализации приложения:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



В следующем коде показано, как можно вызвать функцию CoInitialize для указателя управления.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



После вызова функции CoInitialize на управляющем указателе у вас есть ссылка на этот элемент управления и у него есть доступ к методам элемента управления. Например, можно включить расширенный набор элементов управления, как показано в следующем примере.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Отображение элемента управления

Элемент управления не будет автоматически отображаться после его создания. Чтобы отобразить элемент управления, вызовите метод " [**отобразить**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) " для ссылки на элемент управления, созданной на предыдущем шаге. В следующем коде показано, как можно вызвать метод [**представления**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) .


```
   hr = g_spMIC->Show();
   
```



После того как элемент управления отобразится, он будет выглядеть примерно так, как показано на следующем рисунке.

![снимок экрана с элементом управления математическими данными](images/mic.png)

Обратите внимание, что я включил расширенный набор кнопок, чтобы были доступны **операции** **повтора** и Отмена.

 

 
