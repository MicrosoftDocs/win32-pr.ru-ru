---
description: .
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Начало работы с графикой DirectX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5278e759ea0faf04ac8b247ad3ea1c687dd205c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104080874"
---
# <a name="getting-started-with-directx-graphics"></a>Начало работы с графикой DirectX

Microsoft DirectX Graphics предоставляет набор интерфейсов API, которые можно использовать для создания игр и других высокопроизводительных мультимедийных приложений. DirectX Graphics поддерживает высокопроизводительные высокопроизводительные и трехмерные графики.

Для трехмерной графики используйте API Microsoft Direct3D 11. Даже при наличии аппаратного обеспечения Microsoft Direct3D 9-Level или Microsoft Direct3D 10, вы можете использовать API Direct3D 11 и ориентироваться на устройство [уровня "](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x" или "Feature" 10 \_ x. Сведения о разработке трехмерной графики с помощью DirectX см. в статье [Создание трехмерной графики с помощью DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

Для двухмерной графики и текста используйте Direct2D и [DirectWrite](./directwrite/direct-write-portal.md) , а не Windows интерфейс графических устройств (GDI).

Чтобы создать точечные рисунки, заполненные Direct3D 11 или Direct2D, используйте [DirectComposition](./directcomp/directcomposition-portal.md).

Дополнительные сведения о создании приложения для Магазина Windows, использующего DirectX, см. в статье [Создание первого приложения для Магазина Windows с помощью DirectX](/previous-versions/windows/apps/br229580(v=win.10)
). Вы можете использовать класс [**Windows. UI:: XAML:: Controls:: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) для создания высокопроизводительных приложений DirectX с наложением ПОЛЬЗОВАТЕЛЬСКОГО интерфейса XAML. Дополнительные сведения о сочетании XAML и DirectX в приложении Windows см. в разделе [взаимодействие DirectX и XAML](/previous-versions/windows/apps/hh825871(v=win.10)).

Дополнительные сведения о создании видеодрайверов для Windows 8 см. в разделе [Путеводитель по модели видеодрайверов Windows (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Если вам нужна документация по предыдущим версиям DirectX, см. раздел [Классическая графика DirectX](/windows/desktop/classic-directx-graphics).


 

 
