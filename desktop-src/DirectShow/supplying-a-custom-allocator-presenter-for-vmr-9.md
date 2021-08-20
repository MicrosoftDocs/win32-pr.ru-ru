---
description: Предоставление пользовательского Allocator-Presenter для VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Предоставление пользовательского Allocator-Presenter для VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21e5f87aaecf0b2e8576b60a2d0f6a8c74e60fcf0759a123015ded9136c079bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951723"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Предоставление пользовательского Allocator-Presenter для VMR-9

Чтобы использовать пользовательский распределитель-представление с фильтром визуализации 9 (VMR-9), выполните следующие действия.

1.  Реализуйте класс, который поддерживает интерфейсы [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) и [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) .
2.  Вызовите **QueryInterface** в фильтре VMR-9 для интерфейса [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
3.  Вызовите метод [**IVMRFilterConfig9:: сетрендерингмоде**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) и передайте флаг **VMR9Mode для \_ прорисовки** .
4.  **QueryInterface** в фильтре VMR-9 для интерфейса [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) .
5.  Вызовите метод [**IVMRSurfaceAllocatorNotify9:: адвисесурфацеаллокатор**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) и передайте указатель на метод [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) для распределителя-Presenter.
6.  Вызовите метод [**IVMRSurfaceAllocator9:: адвисенотифи**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) распределителя-Presenter и передайте указатель на интерфейс [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) фильтра VMR-9.
7.  В реализации [**IVMRSurfaceAllocator9:: адвисенотифи**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify)вызовите [**IVMRSurfaceAllocatorNotify9:: SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) , передав указатель на устройство Direct3D и маркер монитора, в котором будет отображаться видео.
8.  В реализации метода [**IVMRSurfaceAllocator9:: Инитиализедевице**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) создайте поверхности Direct3D, соответствующие параметрам, заданным в методе **инитиализедевице** . При необходимости можно использовать метод [**IVMRSurfaceAllocatorNotify9:: аллокатесурфацехелпер**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) фильтра VMR-9, чтобы выделить эти поверхности. Храните указатели поверхности в массиве.
    > [!Note]  
    > Если вы хотите, чтобы кадр-9 нарису кадры видео на поверхность текстуры, добавьте флаг **VMR9AllocFlag \_ текстуресурфаце** в структуру [**VMR9AllocationInfo**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) . Если устройство не поддерживает текстуры в собственном видеоформате, может потребоваться создать отдельную поверхность текстуры, а затем скопировать видеоматериалы из видеоповерхности в текстуру.

     

9.  Во время потоковой передачи VMR-9 получает поверхности из распределителя-Presenter, вызывая метод [**IVMRSurfaceAllocator9::**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) . VMR-9 указывает поверхность по индексу в массиве поверхностей (шаг 8).
10. Представьте изображение, когда VMR-9 вызывает метод [**IVMRImagePresenter9::P ресентимаже**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) . Параметры включают указатель на поверхность Direct3D, содержащую изображение видео.
11. Если устройство Direct3D будет потеряно в любое время, устройство распределителя должно восстановить его и заново создать поверхности. Например, устройство может быть потеряно при изменении режима отображения или когда пользователь перемещает окно на другой монитор. При изменении устройства Direct3D вызовите метод [**IVMRSurfaceAllocatorNotify9:: ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) фильтра VMR-9.
12. При остановке потоковой передачи VMR-9 вызывает метод [**IVMRSurfaceAllocator9:: терминатедевице**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) . Распределитель-выступающий должен освободить все ресурсы Direct3D.

Существуют некоторые различия между VMR-7 и VMR-9 в способе управления пользовательскими распределителями-выступающими:

-   Метод [**аллокатесурфацехелпер**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) фильтра VMR-9 доступен для использования распределителя-Presenter при выделении поверхностей. Этот метод не нужен для пользовательского распределителя, чтобы перенаправить любые вызовы в распределитель-представление по умолчанию. По этой причине идентификатор CLSID фильтра VMR-9 не публикуется по умолчанию для распределителя-Presenter.
-   В отличие от VMR-7, VMR-9 не предоставляет специальный эксклюзивный распределитель режима DirectDraw. Метод [**IVMRSurfaceAllocatorNotify9:: аллокатесурфацехелпер**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) делает этот объект ненужным.
-   Для видео с чередованием VMR-9 всегда переводится в режим чередования, прежде чем изображение будет представлено. Распределитель-выступающий больше не отвечает за дечередование образа перед его отображением.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Режим воспроизведения VMR (пользовательский распределитель — выступающие)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



