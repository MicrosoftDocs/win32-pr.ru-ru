---
description: В этом разделе содержатся сведения о создании объекта индексатора по умолчанию, предоставляемого Media Foundation.
ms.assetid: 3a2caf11-808b-4910-b83c-a272a026f0d3
title: Создание и Настройка индексатора
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0a341e3074ca44aa4403a3f2f518b4fb9082d4c6eadee1f4ca94a69e17bd98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061204"
---
# <a name="indexer-creation-and-configuration"></a>Создание и Настройка индексатора

*ИНДЕКСАТОР* ASF — это компонент уровня вмконтаинер, который используется для чтения или записи объектов индекса в файле ASF. В этом разделе содержатся сведения о создании объекта индексатора по умолчанию, предоставляемого Media Foundation.

Сведения о структуре файла ASF см. в разделе [Структура файлов ASF](asf-file-structure.md).

**Создание и инициализация индексатора ASF**

1.  Вызовите функцию [**мфкреатеасфиндексер**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreateasfindexer) , чтобы получить указатель [**имфасфиндексер**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfindexer) на объект индексатора.
2.  Вызовите метод [**имфасфиндексер:: сетфлагс**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-setflags) , чтобы указать режим чтения или записи для объекта индексатора. По умолчанию индексатор настроен для прямого поиска.

    

    | Назначение                       | Флаг                                           |
    |---------------------------|------------------------------------------------|
    | Чтение (прямой поиск) | Ноль (по умолчанию)                                 |
    | Чтение (обратная попытка поиска) | **\_Чтение индексатора \_ мфасф \_ для \_ реверсеплайбакк** |
    | Запись                   | МФАСФный \_ индексатор \_ записи \_ нового \_ индекса              |

    

     

    > [!Note]  
    > Один и тот же экземпляр индексатора нельзя использовать как для чтения, так и для записи. Необходимо настроить индексатор для одного или другого.

     

3.  Вызовите метод [**имфасфиндексер:: Initialize**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfindexer-initialize) для инициализации индексатора, указав указатель [**имфасфконтентинфо**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfcontentinfo) объекта контентинфо, который описывает файл, который необходимо записать или прочитать. Объект Контентинфо содержит сведения, составляющие [объект заголовка ASF](asf-file-structure.md). Перед созданием или чтением записей индекса ASF-файла объект индексатора требует допустимый объект Контентинфо.

В следующем примере кода показано, как приложение может создать и инициализировать объект индексатора для работы с конкретным содержимым ASF. Объект Контентинфо представляет объект заголовка ASF; содержимое передается в виде потока байтов.


```C++
HRESULT CreateASFIndexer(
    IMFASFContentInfo* pContentInfo, 
    DWORD dwFlags,
    IMFASFIndexer** ppIndexer
    )
{
    *ppIndexer = NULL;

    IMFASFIndexer *pIndexer = NULL;

    HRESULT hr = MFCreateASFIndexer(&pIndexer);
    if (FAILED(hr))
    {
        goto done;
    }

    hr = pIndexer->SetFlags(dwFlags);
    if (FAILED(hr))
    {
        goto done;
    }

    hr =  pIndexer->Initialize(pContentInfo);
    if (FAILED(hr))
    {
        goto done;
    }

    // Return the object to the caller.
    *ppIndexer = pIndexer;
    (*ppIndexer)->AddRef();

done:
    // Clean up.
    SafeRelease(&pIndexer);
    return hr;
}
```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Индексатор ASF](asf-index-object.md)
</dt> <dt>

[Использование индексатора для поиска в файле ASF](using-the-indexer-to-seek.md)
</dt> <dt>

[Использование индексатора для записи нового индекса](using-the-indexer-to-write-a-new-index.md)
</dt> </dl>

 

 



