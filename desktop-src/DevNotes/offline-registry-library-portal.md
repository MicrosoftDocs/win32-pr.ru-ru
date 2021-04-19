---
description: .
ms.assetid: 5861e0a9-6a3f-4bc8-ae8b-d51c9de28217
title: Библиотека автономных разделов реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a473bde729a0047a56d7ad0fdec1c0e3133ea103
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662071"
---
# <a name="offline-registry-library"></a>Библиотека автономных разделов реестра

## <a name="purpose"></a>Назначение

Библиотека автономных разделов реестра (Offreg.dll) используется для изменения куста реестра за пределами активного системного реестра. Эта библиотека предназначена для сценариев обновления реестра, таких как обслуживание образа операционной системы. Библиотека поддерживает форматы кустов реестра, начиная с Windows Vista.

## <a name="developer-audience"></a>Аудитория разработчиков

Эта технология предназначена для изготовителей оборудования (OEM), антивирусных и антивредоносных программ, а также для других разработчиков приложений, которые должны иметь возможность анализировать файлы Hive реестра, не загружая их в активный реестр.

## <a name="run-time-requirements"></a>Требования к среде выполнения

Автономная библиотека реестра предоставляется в виде библиотеки динамической компоновки (DLL), распространяемой в виде двоичного файла. Эта библиотека работает на следующих версиях Windows:

<dl> Windows Server 2016  
Windows 10  
Windows 8.1  
Windows Server 2012 R2  
Windows 8  
Windows Server 2012  
Windows 7  
Windows Server 2008 R2  
Windows Server 2008  
Windows Vista  
</dl>

Приложения должны ссылаться на Offreg.dll с помощью динамической компоновки.

Offreg.dll предоставляется в комплекте драйверов Windows (WDK) для Windows 10 и более ранних версий операционной системы Windows.

Сведения о получении WDK см. в статье [как получить WDK и Влк](/windows-hardware/drivers/download-the-wdk) или посетить веб-сайт [подписок MSDN](https://msdn.microsoft.com/subscriptions/default.aspx) .

## <a name="in-this-section"></a>Содержание раздела

-   [**Сведения о библиотеке автономных разделов реестра**](about-the-offline-registry-library.md)
-   [**Функции библиотеки автономного реестра**](offline-registry-library-functions.md)

 

 
