---
description: Справочный раздел по элементу управления InkPicture для планшетных ПК.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Элемент управления InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef9cb4b5e1919e111e84cc6b654b56b14eff93cfb5aedacc15400fb3ef1af07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451103"
---
# <a name="inkpicture-control"></a>Элемент управления InkPicture

Элемент управления [InkPicture](inkpicture-control-reference.md) позволяет поместить изображение (.jpg, .bmp, .png или Формат .gif) в приложение, к которому пользователи могут добавлять рукописные данные. Он предназначен для сценариев, в которых рукописный ввод не должен распознаться как текст, но хранится в виде рукописного текста.

Пользователи добавляют рукописный ввод в прозрачный слой с помощью пера. Пользователи могут изменять размер окна [InkPicture](inkpicture-control-reference.md) без потери каких-либо сведений о рукописных данных, даже если они обрезаны при изменении размера.

Элемент управления [InkPicture](inkpicture-control-reference.md) включает базовую поддержку печати; Тем не менее, вам нужно реализовать предварительный просмотр или другие расширенные возможности печати.

управляемая (платформа .NET Framework) реализация [InkPicture](/previous-versions/ms583740(v=vs.100)) наследуется от класса [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .

По умолчанию рукописные данные выделяются черным цветом, если они не находятся в режиме высокой контрастности. в противном случае для него задается значение текущий параметр системного цвета (ЦВЕТовая \_ WINDOWTEXT). Кроме того, по умолчанию [**фиттокурве**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) имеет **значение false**.

В элементе управления [InkPicture](inkpicture-control-reference.md) используйте объект [**Ink**](inkdisp-class.md) для загрузки и сохранения рукописного ввода.

> [!Note]  
> Если задать для [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) значение **Delete** или **SELECT**, активируются другие события (например, событие [**Stroke**](inkpicture-stroke.md) ). Эти события полезны, если требуется реализовать собственные режимы удаления или выбора.

 

Подробные справочные сведения о элементе управления [InkPicture](inkpicture-control-reference.md) см. в разделе InkPicture.

В следующих разделах подробно описано использование элемента управления [InkPicture](inkpicture-control-reference.md) :

-   [Работа с изображениями](working-with-pictures.md)
-   [Использование функции InkPicture в более ранних версиях Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
