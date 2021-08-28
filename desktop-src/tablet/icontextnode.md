---
description: Представляет узел в дереве объектов, созданных в ходе анализа рукописного ввода.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Интерфейс Иконтекстноде (Иаком. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 9e6ca9e65b7c14f1df3af00acece8e2ba37c85d6a2193989ab232839f1863c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713472"
---
# <a name="icontextnode-interface"></a>Интерфейс Иконтекстноде

Представляет узел в дереве объектов, созданных в ходе анализа рукописного ввода.

## <a name="members"></a>Элементы

Интерфейс **иконтекстноде** наследует от интерфейса [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **Иконтекстноде** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **иконтекстноде** содержит следующие методы.



| Метод                                                                                  | Описание                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддконтекстлинк**](icontextnode-addcontextlink.md)                                   | Добавляет новый [**иконтекстлинк**](icontextlink.md) в коллекцию ссылок контекста объекта **иконтекстноде** .<br/>                                                                                                          |
| [**аддпропертидата**](icontextnode-addpropertydata.md)                                 | Добавляет часть данных для конкретного приложения.<br/>                                                                                                                                                                         |
| [**Подтвердить**](icontextnode-confirm.md)                                                 | Изменяет тип подтверждения, который управляет тем, что объект [**иинканализер**](iinkanalyzer.md) может измениться о **иконтекстноде**.<br/>                                                                         |
| [**контаинспропертидата**](icontextnode-containspropertydata.md)                       | Определяет, содержит ли объект **иконтекстноде** данные, хранящиеся по указанному идентификатору.<br/>                                                                                                                |
| [**креатепартиаллипопулатедсубноде**](icontextnode-createpartiallypopulatedsubnode.md) | Создает дочерний объект **иконтекстноде** , который содержит только сведения о типе, идентификаторе и расположении.<br/>                                                                                                          |
| [**креатесубноде**](icontextnode-createsubnode.md)                                     | Создает новый дочерний объект **иконтекстноде** .<br/>                                                                                                                                                                       |
| [**делетеконтекстлинк**](icontextnode-deletecontextlink.md)                             | Удаляет объект [**иконтекстлинк**](icontextlink.md) из коллекции ссылок объекта **иконтекстноде** .<br/>                                                                                                         |
| [**делетесубноде**](icontextnode-deletesubnode.md)                                     | Удаляет дочерний элемент **иконтекстноде**.<br/>                                                                                                                                                                                  |
| [**жетконтекстлинкс**](icontextnode-getcontextlinks.md)                                 | Извлекает коллекцию объектов [**иконтекстлинк**](icontextlink.md) , представляющих связи с другими объектами **иконтекстноде** .<br/>                                                                          |
| [**GetId**](icontextnode-getid.md)                                                     | Возвращает идентификатор для объекта **иконтекстноде** .<br/>                                                                                                                                                          |
| [**Нахождения**](icontextnode-getlocation.md)                                         | Извлекает расположение и размер объекта **иконтекстноде** .<br/>                                                                                                                                                    |
| [**жетпарентноде**](icontextnode-getparentnode.md)                                     | Возвращает родительский узел этого **иконтекстноде** в дереве узлов контекста.<br/>                                                                                                                                       |
| [**жетпартиаллипопулатед**](icontextnode-getpartiallypopulated.md)                     | Получает значение, указывающее, является ли объект **иконтекстноде** частично заполнен или полностью заполнен.<br/>                                                                                                   |
| [**жетпропертидата**](icontextnode-getpropertydata.md)                                 | Извлекает данные конкретного приложения или другие данные свойств по заданному идентификатору.<br/>                                                                                                                         |
| [**жетпропертидатаидс**](icontextnode-getpropertydataids.md)                           | Возвращает идентификаторы, для которых имеются данные свойств.<br/>                                                                                                                                                        |
| [**жетстрокекаунт**](icontextnode-getstrokecount.md)                                   | Возвращает число штрихов, связанных с объектом **иконтекстноде** .<br/>                                                                                                                                       |
| [**жетстрокеид**](icontextnode-getstrokeid.md)                                         | Извлекает идентификатор штриха для штриха, на который ссылается значение индекса в объекте **иконтекстноде** .<br/>                                                                                                    |
| [**жетстрокеидс**](icontextnode-getstrokeids.md)                                       | Извлекает массив идентификаторов для штрихов в объекте **иконтекстноде** .<br/>                                                                                                                              |
| [**жетстрокепаккетдатабид**](icontextnode-getstrokepacketdatabyid.md)                 | Извлекает массив, содержащий данные свойства пакета для указанного штриха.<br/>                                                                                                                                   |
| [**жетстрокепаккетдескриптионбид**](icontextnode-getstrokepacketdescriptionbyid.md)   | Извлекает массив, содержащий идентификаторы свойств пакета для указанного росчерка.<br/>                                                                                                                            |
| [**жетсубнодес**](icontextnode-getsubnodes.md)                                         | Возвращает прямые дочерние узлы объекта **иконтекстноде** .<br/>                                                                                                                                                   |
| [**GetType**](icontextnode-gettype.md)                                                 | Возвращает тип объекта **иконтекстноде** .<br/>                                                                                                                                                                 |
| [**Имя_типа**](icontextnode-gettypename.md)                                         | Возвращает удобное для чтения имя типа этого **иконтекстноде**.<br/>                                                                                                                                                     |
| [**Подтверждено**](icontextnode-isconfirmed.md)                                         | Получает значение, указывающее, подтвержден ли объект **иконтекстноде** . [**Иинканализер**](iinkanalyzer.md) не может изменить тип узла и связанные штрихи для подтвержденных объектов **иконтекстноде** .<br/> |
| [**лоадпропертиесдата**](icontextnode-loadpropertiesdata.md)                           | Повторно создает данные о свойстве и внутренних свойствах приложения для массива байтов, созданного ранее с помощью [**иконтекстноде:: савепропертиесдата**](icontextnode-savepropertiesdata.md).<br/>                  |
| [**мовесубнодетопоситион**](icontextnode-movesubnodetoposition.md)                     | Переупорядочивает указанный дочерний объект **иконтекстноде** по указанному индексу.<br/>                                                                                                                                         |
| [**ремовепропертидата**](icontextnode-removepropertydata.md)                           | Удаляет часть данных, зависящих от приложения.<br/>                                                                                                                                                                      |
| [**Переподчинить**](icontextnode-reparent.md)                                               | Перемещает этот объект **иконтекстноде** из коллекции подузлов родительского узла контекста в коллекцию подузлов указанного узла контекста.<br/>                                                                         |
| [**репарентстрокебидтоноде**](icontextnode-reparentstrokebyidtonode.md)               | Перемещает данные штриха из этого **иконтекстнодеа** в указанный **иконтекстноде**.<br/>                                                                                                                                    |
| [**савепропертиесдата**](icontextnode-savepropertiesdata.md)                           | Извлекает массив байтов, содержащий данные внутреннего свойства и внутренних свойств для данного **иконтекстноде**.<br/>                                                                                           |
| [**SetLocation**](icontextnode-setlocation.md)                                         | Обновляет расположение и размер этого **иконтекстноде**.<br/>                                                                                                                                                            |
| [**сетпартиаллипопулатед**](icontextnode-setpartiallypopulated.md)                     | Изменяет значение, указывающее, является ли **иконтекстноде** частично или полностью заполненным.<br/>                                                                                                                   |
| [**сетстрокес**](icontextnode-setstrokes.md)                                           | Связывает указанные штрихи с этим **иконтекстноде**.<br/>                                                                                                                                                       |



 

## <a name="remarks"></a>Remarks

Типы узлов описаны в константах [типов узлов контекста](context-node-types.md) .

## <a name="examples"></a>Примеры

В следующем примере показан метод, который проверяет **иконтекстноде**; метод выполняет следующие действия:

-   Возвращает тип узла контекста. Если контекстный узел является неклассифицированным рукописным вводом, указанием анализа или узлом пользовательского распознавателя, он вызывает вспомогательный метод для проверки конкретных свойств типа узла.
-   Если узел содержит подузлы, он проверяет каждый подузел, вызывая сам себя.
-   Если узел является листовым узлом рукописного ввода, он проверяет данные штриха для узла, вызывая вспомогательный метод.

API положение Инканалисис позволяет создать узел линии, содержащий рукописные слова и текстовые слова. Однако синтаксический анализатор будет игнорировать эти смешанные узлы и будет обрабатывать их как внешние узлы. Это повлияет на точность анализа при обнаружении рукописных заметок, когда пользователь выполняет запись или вокруг этого смешанного узла.


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows XP Tablet PC Edition \[ только классические приложения\]<br/>                                                 |
| Минимальная версия сервера<br/> | Ни одна версия не поддерживается<br/>                                                                                     |
| Заголовок<br/>                   | <dl> <dt>Иаком. h (также требуется Иаком \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**иконтекстнодес**](icontextnodes.md)
</dt> <dt>

[Типы узлов контекста](context-node-types.md)
</dt> <dt>

[**иинканализер**](iinkanalyzer.md)
</dt> <dt>

[Справочник по анализу рукописного ввода](ink-analysis-reference.md)
</dt> </dl>

 

