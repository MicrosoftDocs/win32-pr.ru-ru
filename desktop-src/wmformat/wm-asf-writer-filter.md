---
title: Фильтр модуля записи WM ASF (пакет SDK для формата Windows Media 11)
description: Фильтр модуля записи WM ASF
ms.assetid: a902c92e-836d-492c-b2d2-89c216125774
keywords:
- Windows Media Format SDK, модуль записи WM ASF
- DirectShow, модуль записи WM ASF
- Фильтры КАСФ, модуль записи WM ASF
- Модуль записи WM ASF, сведения
- Расширенный формат систем (ASF), модуль записи WM ASF
- ASF (Расширенный системный формат), модуль записи WM ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d0de34bcf4b4047673f832d78f40377f98e94d6
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "105681722"
---
# <a name="wm-asf-writer-filter-windows-media-format-11-sdk"></a>Фильтр модуля записи WM ASF (пакет SDK для формата Windows Media 11)

Фильтр модуля записи WM ASF принимает переменное число входных потоков и создает файл ASF. Фильтр обрабатывает все сжатие и мультиплексирование (хотя механизм сжатия можно обойти). Фильтр модуля записи WM ASF можно использовать в различных сценариях, включая видеозапись цифрового видео (DV), повторное сжатие звука и преобразование Audio-Video файлов с чередованием (AVI) или файлы мультимедиа MPEG для сетевой потоковой передачи. Этот фильтр предоставляет единственный способ создания видеофайлов Microsoft Windows Media Audio и Windows Media в DirectShow.

Дополнительные сведения см. [в разделе Создание файлов ASF в DirectShow](creating-asf-files-in-directshow.md).

В следующей таблице содержатся сведения о фильтре модуля записи WM ASF, например интерфейсах и типах носителей, которые он поддерживает.



|                        |                                                                                                                                                                                                                         |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Интерфейсы фильтра      | **Иамфилтермискфлагс**, **ибасефилтер**, **иконфигасфвритер**, **IFileSinkFilter2**, Имедиасикинг, IPersistStream, IServiceProvider, испеЦифипропертипажес, **IWMIndexer2**, **IWMHeaderInfo**, **IWMWriterAdvanced2** |
| Типы носителей входных закрепления  | Зависит от профиля. Обычно это несжатые типы, такие как MEDIATYPE \_ Audio или MediaType \_ Video, хотя сжатые типы могут быть приняты, если они соответствуют профилю.                                                   |
| Интерфейсы входных закрепления   | **Ипин**, **имеминпутпин**, **иамстреамконфиг**, **IServiceProvider**, **иамвмбуфферпасс**, **IWMStreamConfig2** (через **IServiceProvider**)                                                                         |
| Типы носителей для выходного ПИН-кода | Неприменимо                                                                                                                                                                                                          |
| Интерфейсы выходного ПИН-кода  | Неприменимо                                                                                                                                                                                                          |
| Фильтровать CLSID           | \_ВМАСФВРИТЕР CLSID                                                                                                                                                                                                      |
| CLSID страницы свойств    | \_ВМАСФВРИТЕРПРОПЕРТИЕС CLSID                                                                                                                                                                                            |
| Исполняемый объект             | Qasf.dll                                                                                                                                                                                                                |
| Заслуживают                  | \_ \_ не \_ использовать                                                                                                                                                                                                     |
| Категория фильтра        | Не указано                                                                                                                                                                                                           |



 

## <a name="remarks"></a>Комментарии

Количество входных контактов фильтра зависит от профиля, который передается в фильтр. Для каждого потока, определенного в профиле, создается один ПИН-код соответствующего типа носителя.

Входные сигналы поддерживают один метод из интерфейса **иамстреамконфиг** : **иамстреамконфиг::-Format**. Все остальные методы возвращают E \_ нотимпл. Вызовите метод **OnFormat** , чтобы запросить формат сжатия целевого объекта ПИН-кода, который определяется текущим профилем. Чтобы задать профиль, используйте интерфейс [**иконфигасфвритер**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85)) .

Интерфейс **IServiceProvider** фильтра позволяет приложениям получать интерфейс [**IWMWriterAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced2) , который определен в пакете SDK формата Windows Media. Интерфейс **IWMWriterAdvanced2** управляет дечередованием видео и полезен, если входные данные представляют собой [*чередующийся*](wmformat-glossary.md) источник, например DV (цифровое видео). Используйте методы **жетинпутсеттинг** и **сетинпутсеттинг** для управления разчередованием. Не рекомендуется, чтобы клиенты использовали другие методы этого интерфейса. Этот интерфейс можно получить только после добавления фильтра к графу фильтра. В следующем примере показано, как запросить этот интерфейс:


```C++
// Assume that m_pGraph is a valid IGraphBuilder interface pointer,
// and that pAsfWriter points to the IBaseFilter interface
// on the WM ASF Writer filter.

IServiceProvider *pProvider = NULL;
IWMWriterAdvanced2 *pWMWA2 = NULL;

hr = m_pGraph->AddFilter(pAsfWriter, L"WM ASF Writer");
...
hr = pAsfWriter->QueryInterface(IID_IServiceProvider, (void**)&pProvider)
if (SUCCEEDED(hr))
{
    hr = pProvider->QueryService(IID_IWMWriterAdvanced2,
        IID_IWMWriterAdvanced2, (void**)&pWMWA2);
    pProvider->Release();
}

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Справочник по КАСФ DirectShow**](directshow-qasf-reference.md)
</dt> </dl>

 

 
