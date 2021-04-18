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
# <a name="com-library-and-activex-controls"></a>Библиотека COM и элементы управления ActiveX

В этом разделе описывается настройка среды для использования библиотек COM платформы Tablet PC в C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

Чтобы создать приложения для планшетных ПК в Visual C++, необходимо обновить системные переменные среды, настроить параметры каталога для Visual Studio и получить доступ к интерфейсам планшетных ПК в проекте.

Чтобы обновить переменные среды, следуйте инструкциям, приведенным в Windows SDK для добавления переменных среды в Visual Studio.

### <a name="accessing-the-tablet-pc-interfaces"></a>Доступ к интерфейсам планшетных ПК

Для доступа к интерфейсам планшетных ПК необходимо включить в проект файлы Мсинкаут. h и Мсинкаут \_ i. c.


```C++
#include <msinkaut.h>
#include <msinkaut_i.c>
```



Можно также использовать следующую директиву импорта вместо \# инструкций include, перечисленных выше.


```C++
#import "InkObj.dll" no_namespace exclude("tagXFORM")
```



Для доступа к интерфейсам Инканалисис необходимо включить в проект файлы Иаком. h и Иаком \_ i. c.


```C++
#include <IACom.h>
#include <IACom_i.c>
```



Можно также использовать следующую директиву импорта вместо \# инструкций include, перечисленных выше.


```C++
#import "IACom.dll" no_namespace exclude("tagXFORM")
```



Для доступа к интерфейсам [**инкдивидер**](inkdivider-class.md) необходимо включить \_ в проект файлы msinkaut15 i. c и msinkaut15. h.

> [!Note]  
> Инкдивидер был заменен API-интерфейсами анализа рукописного ввода.

 


```C++
#include <msinkaut15.h>
#include <msinkaut15_i.c>
```



Можно также использовать следующую директиву импорта вместо \# инструкций include.


```C++
#import "InkDiv.dll" no_namespace exclude("tagXFORM")
```



Для доступа к интерфейсам [**пенинпутпанел**](peninputpanel-class.md) необходимо включить \_ в проект файлы пенинпутпанел i. c и пенинпутпанел. h.


```C++
#include <PenInputPanel.h>
#include <PenInputPanel_i.c>
```



Можно также использовать следующую директиву импорта вместо \# инструкций include.


```C++
#import "PIPanel.dll" no_namespace 
```



> [!Note]  
> Интерфейсы API Пенинпутпанел были заменены в Windows Vista новыми интерфейсами панели ввода текста.

 

Для доступа к интерфейсам элемента управления [InkEdit](inkedit-control-reference.md) необходимо включить в проект файлы с заданными. h и \_ i. c.


```C++
#include <inked.h>
#include <inked_i.c>
```



Кроме того, можно \# импортировать файл InkEd.dll.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



