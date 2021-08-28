---
description: В этом разделе описывается настройка среды для использования библиотек COM платформы Tablet PC в C++.
ms.assetid: c0d7f703-d4aa-4c26-ae81-a4c888383c1e
title: библиотека COM и элементы управления ActiveX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78bc76f9caa2bcb72fe26ed2e01e251c977f87ce01c12794aad78608d2f5887f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009094"
---
# <a name="com-library-and-activex-controls"></a>библиотека COM и элементы управления ActiveX

В этом разделе описывается настройка среды для использования библиотек COM платформы Tablet PC в C++.

## <a name="microsoft-visual-c"></a>Microsoft Visual C++

чтобы создать приложения для планшетных пк в Visual C++, необходимо обновить системные переменные среды, настроить параметры каталога для Visual Studio и получить доступ к интерфейсам планшетных пк в проекте.

чтобы обновить переменные среды, следуйте инструкциям, приведенным в Windows SDK для добавления переменных среды в Visual Studio.

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
> интерфейсы api пенинпутпанел были заменены в Windows Vista новыми интерфейсами панели ввода текста.

 

Для доступа к интерфейсам элемента управления [InkEdit](inkedit-control-reference.md) необходимо включить в проект файлы с заданными. h и \_ i. c.


```C++
#include <inked.h>
#include <inked_i.c>
```



Кроме того, можно \# импортировать файл InkEd.dll.


```C++
#import "InkEd.dll" no_namespace exclude("tagXFORM")
```



 

 



