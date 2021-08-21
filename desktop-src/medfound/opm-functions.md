---
description: В выходных данных диспетчера защиты (ОПМ) используются следующие функции.
ms.assetid: 7ecde6ae-56fd-451b-bebb-224c6801be05
title: Функции ОПМ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3de880584716c5caac94c93e48dd89ded481c14e1c7a08be3e23ac334e1c8bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118058768"
---
# <a name="opm-functions"></a>Функции ОПМ

В [выходных данных диспетчера защиты](output-protection-manager.md) (ОПМ) используются следующие функции.



| Функция                                                                                             | Описание                                                                                                                           |
|------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**опмжетвидеуутпутфортаржет**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputfortarget)                                     | Возвращает объект вывода видео для целевого объекта VidPN на указанном адаптере.                                                          |
| [**опмжетвидеуутпутсфромхмонитор**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromhmonitor)                             | Создает объект диспетчера выходной защиты (ОПМ) для каждого физического монитора, связанного с определенным маркером **хмонитор** . |
| [**OPMGetVideoOutputsFromIDirect3DDevice9Object**](/windows/desktop/api/opmapi/nf-opmapi-opmgetvideooutputsfromidirect3ddevice9object) | Создает объект ОПМ для каждого физического монитора, связанного с определенным устройством Direct3D.                                 |



 

Для доступа к функциям в драйвере экрана используются следующие функции ОПМ. Приложения не должны вызывать эти функции.

-   [**конфигуреопмпротектедаутпут**](configureopmprotectedoutput.md)
-   [**креатеопмпротектедаутпутс**](createopmprotectedoutputs.md)
-   [**дестройопмпротектедаутпут**](destroyopmprotectedoutput.md)
-   [**Метода getcertificate**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificate)
-   [**жетцертификатесизе**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-getcertificatesize)
-   [**жеткоппкомпатиблеопминформатион**](getcoppcompatibleopminformation.md)
-   [**жетопминформатион**](getopminformation.md)
-   [**жетопмрандомнумбер**](getopmrandomnumber.md)
-   [**жетсугжестедопмпротектедаутпутаррайсизе**](getsuggestedopmprotectedoutputarraysize.md)
-   [**сетопмсигнингкэйандсекуенценумберс**](setopmsigningkeyandsequencenumbers.md)

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Справочник по программированию ОПМ](opm-programming-reference.md)
</dt> <dt>

[Диспетчер выходной защиты](output-protection-manager.md)
</dt> </dl>

 

 



