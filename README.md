# In2Sport Rooster scraper / viewer

To scrape the rooster and get JS objects:
```js
const trainings = Array.from(document.querySelectorAll('.evtitem')).map(el => {
    return {
        title: el.querySelector('.title').innerText,
        time: el.querySelector('.time').innerText,
        trainer: el.querySelector('.trainer').innerText,
        attendees: el.querySelector('.attendees').innerText,
    }
});

const basicTrainings = trainings.filter(training => training.title.toLowerCase().includes('basic'));
```